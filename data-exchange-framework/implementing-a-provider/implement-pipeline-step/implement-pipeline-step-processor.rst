Implement Pipeline Step Processor
=======================================

A *processor* is needed to implement the business logic for the 
*pipeline step*. The pipeline step has an *endpoint* assigned to
it. The converter has put this endpoint into a *plugin* on the
pipeline step.

The processor uses this plugin to get a reference to the endpoint.
Once it has the endpoint, it can get the path to the file that is
configured on the endpoint.

Next the processor reads the file, line by line. For each line,
it splits the line into an array, using the separator specified
on the endpoint.

Each array of values is added to a collection. This collection is
added to the *pipeline context* so that a subsequent pipeline step
can handle the data.

    .. important:: 
    
        This pipeline step reads all of the files in the file identified
        the the endpoint. This means multiple "records" are being read
        (each line in the file is a separate "record").

        When a pipeline step reads multiple records from an endpoint, the
        convention in Data Exchange Framework is that those records are
        added to the pipeline context so a subsequent pipeline step
        can handle the data.

        While the convention exists so that people can make an educated 
        guess that another pipeline step is needed to handle the data,
        but people cannot guess what format that data will be in.

        Therefore, it is critical that you provide documentation 
        along with your provider.

1. In Visual Studio, add the following class:

    .. code-block:: c#
    
        using Sitecore.DataExchange.Attributes;
        using Sitecore.DataExchange.Contexts;
        using Sitecore.DataExchange.Models;
        using Sitecore.DataExchange.Plugins;
        using Sitecore.DataExchange.Processors.PipelineSteps;
        using Sitecore.DataExchange.Providers.FileSystem.Plugins;
        using System;
        using System.IO;

        namespace Examples.FileSystem.Processors.PipelineSteps
        {
            [RequiredEndpointPlugins(typeof(TextFileSettings))]
            public class ReadTextFileStepProcessor : BaseReadDataStepProcessor
            {
                public ReadTextFileStepProcessor()
                {
                }
                protected override void ReadData(
                    Endpoint endpoint, 
                    PipelineStep pipelineStep, 
                    PipelineContext pipelineContext)
                {
                    if (endpoint == null)
                    {
                        throw new ArgumentNullException(nameof(endpoint));
                    }
                    if (pipelineStep == null)
                    {
                        throw new ArgumentNullException(nameof(pipelineStep));
                    }
                    if (pipelineContext == null)
                    {
                        throw new ArgumentNullException(nameof(pipelineContext));
                    }
                    var logger = pipelineContext.PipelineBatchContext.Logger;
                    //
                    //get the file path from the plugin on the endpoint
                    var settings = endpoint.GetTextFileSettings();
                    if (settings == null)
                    {
                        return;
                    }
                    if (string.IsNullOrWhiteSpace(settings.Path))
                    {
                        logger.Error(
                            "No path is specified on the endpoint. " + 
                            "(pipeline step: {0}, endpoint: {1})", 
                            pipelineStep.Name, endpoint.Name);
                        return;
                    }
                    if (!File.Exists(settings.Path))
                    {
                        logger.Error(
                            "The path specified on the endpoint does not exist. " + 
                            "(pipeline step: {0}, endpoint: {1}, path: {2})",
                            pipelineStep.Name, endpoint.Name, settings.Path);
                        return;
                    }
                    //
                    //read the file, one line at a time
                    var separator = new string[] { settings.ColumnSeparator };
                    var lines = new List<string[]>();
                    using (var reader = new StreamReader(File.OpenRead(settings.Path)))
                    {
                        var firstLine = true;
                        while(!reader.EndOfStream)
                        {
                            var line = reader.ReadLine();
                            if (firstLine && settings.ColumnHeadersInFirstLine)
                            {
                                firstLine = false;
                                continue;
                            }
                            if (string.IsNullOrWhiteSpace(line))
                            {
                                continue;
                            }
                            //
                            //split the line into an array, using the separator
                            var values = line.Split(separator, StringSplitOptions.None);
                            lines.Add(values);
                        }
                    }
                    //
                    //add the data that was read from the file to a plugin
                    var dataSettings = new IterableDataSettings(lines);
                    logger.Info(
                        "Rows were read from the file. (pipeline step: {0}, endpoint: {1})", 
                        pipelineStep.Name, endpoint.Name);
                    //
                    //add the plugin to the pipeline context
                    pipelineContext.Plugins.Add(dataSettings);
                }
            }
        }
