Implement Endpoint Converter
===================================================
A converter is needed to convert a Sitecore item that represents
a component into the component. In this example, a converter is
needed to convert the settings on an endpoint item into the 
endpoint settings plugin, and to add that plugin to the endpoint.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.Attributes;
    using Sitecore.DataExchange.Converters.Endpoints;
    using Sitecore.DataExchange.Models;
    using Sitecore.DataExchange.Repositories;
    using Sitecore.Services.Core.Model;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DataExchange.Providers.FileSystem
    {
        [SupportedIds(TextFileEndpointTemplateId)]
        public class TextFileEndpointConverter : BaseEndpointConverter
        {
            public const string TextFileEndpointTemplateId = "[ENDPOINT TEMPLATE ID]";
            public const string TemplateFieldColumnSeparator = "ColumnSeparator";
            public const string TemplateFieldColumnHeadersInFirstLine = "ColumnHeadersInFirstLine";
            public const string TemplateFieldPath = "Path";
            public TextFileEndpointConverter(IItemModelRepository repository) : base(repository)
            {
            }
            protected override void AddPlugins(ItemModel source, Endpoint endpoint)
            {
                //
                //create the plugin
                var settings = new TextFileSettings
                {
                    //
                    //populate the plugin using values from the item
                    ColumnHeadersInFirstLine = this.GetBoolValue(source, TemplateFieldColumnHeadersInFirstLine),
                    ColumnSeparator = this.GetStringValue(source, TemplateFieldColumnSeparator),
                    Path = this.GetStringValue(source, TemplateFieldPath)
                };
                //
                //add the plugin to the endpoint
                endpoint.AddPlugin(settings);
            }
        }
    }

.. important::

    You must change the value of ``[ENDPOINT TEMPLATE ID]`` to match 
    the id from the endpoint template named **Text File Endpoint**.

.. hint::

    By inheriting from `BaseEndpointConverter </component-reference/converters/base-endpoint-converter.html>`_ 
    you get access to a number of methods that facilitate reading 
    values from fields on a Sitecore item.

2. Compile the project.
3. Deploy **Examples.DataExchange.Providers.FileSystem.dll** to the Sitecore server.