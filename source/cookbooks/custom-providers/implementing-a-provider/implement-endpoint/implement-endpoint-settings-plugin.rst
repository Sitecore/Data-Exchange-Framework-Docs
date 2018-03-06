Implement Endpoint Settings Plugin
===================================================
The endpoint settings are configured using the endpoint 
template. In this example, settings such as the path of
the file that can be read and whether the first line of 
the file contains column headers can be configured.

The endpoint template provides design-time access to 
the endpoint settings. Runtime access to the endpoint
settings is provided through plugins. A plugin is needed
to handle the specific settings on the endpoint.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DataExchange.Providers.FileSystem
    {
        public class TextFileSettings : IPlugin
        {
            public TextFileSettings() { }
            public bool ColumnHeadersInFirstLine { get; set; }
            public string ColumnSeparator { get; set; }
            public string Path { get; set; }
        }
    }

2. Add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.Models;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DataExchange.Providers.FileSystem
    {
        public static class EndpointExtensions
        {
            public static TextFileSettings GetTextFileSettings(this Endpoint endpoint)
            {
                return endpoint.GetPlugin<TextFileSettings>();
            }
            public static bool HasTextFileSettings(this Endpoint endpoint)
            {
                return (GetTextFileSettings(endpoint) != null);
            }
        }
    }

.. note::

    This extension method makes it easier to access
    the plugin when it is needed.
    
    Providing extension methods to access a plugin 
    is a best practice to consider when implementing 
    a provider for Data Exchange Framework.