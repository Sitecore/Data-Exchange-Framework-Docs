Implement Pipeline Step Processor
===================================================
A processor is where the business logic for a component 
is implemented. In this example, a processor is needed 
to implement the business logic for the pipeline step
responsible for reading data from the text file that
corresponds to the endpoint assigned to the pipeline step.

A pipeline step does not exist in a vacuum. It is designed
to be a part of a data synchronization process. This means
that the processor for a pipeline step may expect certain
conditions to exist when it runs. In this example, the
processor expects that a plugin **TextFileSettings** is
included in the endpoint's plugin collection.

A processor may also create conditions that subsequent 
pipeline steps expect. In this example, the processor
adds a plugin **IterableDataSettings** to the pipeline
context's plugin collection.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.Attributes;
    using Sitecore.DataExchange.Contexts;
    using Sitecore.DataExchange.Models;
    using Sitecore.DataExchange.Plugins;
    using Sitecore.DataExchange.Processors.PipelineSteps;
    using Sitecore.Services.Core.Diagnostics;
    using System;
    using System.Collections.Generic;
    using System.IO;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DataExchange.Providers.FileSystem
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
                PipelineContext pipelineContext,
                ILogger logger)
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
                if (logger == null)
                {
                    throw new ArgumentNullException(nameof(logger));
                }
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
                //add the data that was read from the file to a plugin
                var data = this.GetIterableData(settings);
                var dataSettings = new IterableDataSettings(data);
                //
                //add the plugin to the pipeline context
                pipelineContext.AddPlugin(dataSettings);
            }
            protected virtual IEnumerable<string[]> GetIterableData(TextFileSettings settings)
            {
                //
                //read the file, one line at a time
                var separator = new string[] { settings.ColumnSeparator };
                using (var reader = new StreamReader(File.OpenRead(settings.Path)))
                {
                    var firstLine = true;
                    while (!reader.EndOfStream)
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
                        yield return values;
                    }
                }
            }
        }
    }

.. hint::

    By inheriting from `BaseReadDataStepProcessor </component-reference/processors/pipeline-steps/base-read-data-step-processor.html>`_ 
    you get access methods that facilitate reading data from an endpoint.

    The base class does not specify what you must do with the data
    that is read. However, most of the time the data is added to
    a plugin **IterableDataSettings** so that a subsequent pipeline
    step processor can iterate the data and handle it in some way.

2. Compile the project.
3. Deploy **Examples.DataExchange.Providers.FileSystem.dll** to the Sitecore server.