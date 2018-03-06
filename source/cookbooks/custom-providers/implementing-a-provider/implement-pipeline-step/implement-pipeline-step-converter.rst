Implement Pipeline Step Converter
===================================================
In this example, a converter is needed to convert the 
settings on a pipeline step item into a plugin that
identifies the endpoint that the pipeline step will
read from.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.Attributes;
    using Sitecore.DataExchange.Converters.PipelineSteps;
    using Sitecore.DataExchange.Models;
    using Sitecore.DataExchange.Plugins;
    using Sitecore.DataExchange.Repositories;
    using Sitecore.Services.Core.Model;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DataExchange.Providers.FileSystem
    {
        [SupportedIds(ReadTextFileStepTemplateId)]
        public class ReadTextFileStepConverter : BasePipelineStepConverter
        {
            public const string ReadTextFileStepTemplateId = "[PIPELINE STEP TEMPLATE ID]";
            public const string TemplateFieldEndpointFrom = "EndpointFrom";
            public ReadTextFileStepConverter(IItemModelRepository repository) : base(repository)
            {
            }
            protected override void AddPlugins(ItemModel source, PipelineStep pipelineStep)
            {
                //
                //create the plugin
                var settings = new EndpointSettings
                {
                    //
                    //populate the plugin using values from the item
                    EndpointFrom = this.ConvertReferenceToModel<Endpoint>(source, TemplateFieldEndpointFrom)
                };
                //
                //add the plugin to the pipeline step
                pipelineStep.AddPlugin(settings);
            }
        }
    }

.. important::

    You must change the value of ``[PIPELINE STEP TEMPLATE ID]`` 
    to match the id from the pipeline step template named 
    **Read Text File Pipeline Step**.

.. hint::

    By inheriting from `BasePipelineStepConverter </component-reference/converters/base-pipeline-step-converter.html>`_ 
    you get access to a number of methods that facilitate reading 
    values from fields on a Sitecore item.

    In addition to being able to read simple values like strings, 
    numbers and dates, methods are available to automatically 
    convert referenced items into the appropriate Data Exchange 
    Framework component.

2. Compile the project.
3. Deploy **Examples.DataExchange.Providers.FileSystem.dll** to the Sitecore server.