Implement Endpoint Converter
=======================================

A *converter* is needed to convert a Sitecore item that represents 
a file system endpoint into an endpoint component for Data Exchange
Framework, and that adds the endpoint settings *plugin* to the 
endpoint component.

1. In Visual Studio, add the following class:

    .. code-block:: c#
    
        using Sitecore.Services.Core.Model;
        using System;

        namespace Examples.FileSystem.Models.ItemModels.Endpoints
        {
            public class TextFileEndpointItemModel : ItemModel
            {
                public const string ColumnSeparator = "ColumnSeparator";
                public const string ColumnHeadersInFirstLine = "ColumnHeadersInFirstLine";
                public const string Path = "Path";
            }
        }
    
    .. note:: 
    
        This class defines constants for the names of the fields from 
        the endpoint template. These field names are referenced by the 
        converter.
        
        In order for the converter to be able to run inside or outside
        of the Sitecore server, the type ``Sitecore.Services.Core.Model.ItemModel``
        is used to represent Sitecore items. Fields on this type are 
        accessed by name.
        
        This stands in contrast to how field are accessed on ``Sitecore.Data.Items.Item``.
        In this type, fields can be accessed by name or ID, with ID 
        being the preferred value since it is unlikely to change.

2. Add the following class:

    .. code-block:: c#

        using Examples.FileSystem.Models.ItemModels.Endpoints;
        using Examples.FileSystem.Plugins;
        using Sitecore.DataExchange.Converters.Endpoints;
        using Sitecore.DataExchange.Models;
        using Sitecore.DataExchange.Repositories;
        using Sitecore.Services.Core.Model;
        using System;
        
        namespace Examples.FileSystem.Converters.Endpoints
        {
            public class TextFileEndpointConverter : BaseEndpointConverter<ItemModel>
            {
                private static readonly Guid TemplateId = Guid.Parse("[ENDPOINT TEMPLATE ID]");
                public TextFileEndpointConverter(IItemModelRepository repository) : base(repository)
                {
                    //
                    //identify the template an item must be based 
                    //on in order for the converter to be able to 
                    //convert the item
                    this.SupportedTemplateIds.Add(TemplateId);
                }
                protected override void AddPlugins(ItemModel source, Endpoint endpoint)
                {
                    //
                    //create the plugin
                    var settings = new TextFileSettings();
                    //
                    //populate the plugin using values from the item
                    settings.ColumnHeadersInFirstLine = 
                        base.GetBoolValue(source, TextFileEndpointItemModel.ColumnHeadersInFirstLine);
                    settings.ColumnSeparator = 
                        base.GetStringValue(source, TextFileEndpointItemModel.ColumnSeparator);
                    settings.Path = 
                        base.GetStringValue(source, TextFileEndpointItemModel.Path);
                    //
                    //add the plugin to the endpoint
                    endpoint.Plugins.Add(settings);
                }
            }
        }

    .. important:: 

        You must change the value of ``[ENDPOINT TEMPLATE ID]`` 
        to match the id from the endpoint template you created
        named **Text File Endpoint**.
        
    .. hint:: 
    
        By inheriting from ``BaseEndpointConverter<ItemModel>`` you  
        get access to a number of methods that facilitate reading 
        values from fields on a Sitecore item. 

        In addition to being able to read simple values like strings,
        numbers and dates, methods are available to automatically 
        convert referenced items into the appropriate Data Exchange
        Framework component.

        See the API documentation for more information.
