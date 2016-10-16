Implement Pipeline Step Converter
=======================================

A *converter* is needed to convert a Sitecore item that represents 
a *pipeline step* that can read from a file system endpoint into a
pipeline step component for Data Exchange Framework, and that adds 
the settings configured on the pipeline step item using the 
appropriate *plugin*.

1. In Visual Studio, add the following class:

    .. code-block:: c#
    
        using Sitecore.Services.Core.Model;
        using System;

        namespace Examples.FileSystem.Models.ItemModels.PipelineSteps
        {
            public class ReadTextFileStepItemModel : ItemModel
            {
                public const string EndpointFrom = "EndpointFrom";
            }
        }
    
    .. note:: 
    
        This class defines constants for the names of the fields from 
        the pipeline step template. These field names are referenced  
        by the converter.
        
        In order for the converter to be able to run inside or outside
        of the Sitecore server, the type ``Sitecore.Services.Core.Model.ItemModel``
        is used to represent Sitecore items. Fields on this type are 
        accessed by name.
        
        This stands in contrast to how field are accessed on ``Sitecore.Data.Items.Item``.
        In this type, fields can be accessed by name or ID, with ID 
        being the preferred value since it is unlikely to change.

2. Add the following class:

    .. code-block:: c#

        using Examples.FileSystem.Models.ItemModels.PipelineSteps;
        using Sitecore.DataExchange.Converters.PipelineSteps;
        using Sitecore.DataExchange.Models;
        using Sitecore.DataExchange.Plugins;
        using Sitecore.DataExchange.Repositories;
        using Sitecore.Services.Core.Model;
        using System;

        namespace Examples.FileSystem.Converters.PipelineSteps
        {
            public class ReadTextFileStepConverter : BasePipelineStepConverter<ItemModel>
            {
                private static readonly Guid TemplateId = Guid.Parse("[PIPELINE STEP TEMPLATE ID]");
                public ReadTextFileStepConverter(IItemModelRepository repository) : base(repository)
                {
                    this.SupportedTemplateIds.Add(TemplateId);
                }
                protected override void AddPlugins(ItemModel source, PipelineStep pipelineStep)
                {
                    AddEndpointSettings(source, pipelineStep);
                }
                private void AddEndpointSettings(ItemModel source, PipelineStep pipelineStep)
                {
                    var settings = new EndpointSettings();
                    var endpointFrom = base.ConvertReferenceToModel<Endpoint>(source, ReadTextFileStepItemModel.EndpointFrom);
                    if (endpointFrom != null)
                    {
                        settings.EndpointFrom = endpointFrom;
                    }
                    pipelineStep.Plugins.Add(settings);
                }
            }
        }

    .. important:: 

        You must change the value of ``[PIPELINE STEP TEMPLATE ID]`` 
        to match the id from the pipeline step template you created
        named **Read Text File Pipeline Step**.
        
    .. hint:: 
    
        By inheriting from ``BaseEndpointConverter<ItemModel>`` you  
        get access to a number of methods that facilitate reading 
        values from fields on a Sitecore item. 

        In addition to being able to read simple values like strings,
        numbers and dates, methods are available to automatically 
        convert referenced items into the appropriate Data Exchange
        Framework component.

        See the API documentation for more information.
