Implement Endpoint Settings Plugin
=======================================

The *endpoint* settings are configured using the endpoint template.
When an endpoint item is converted into an endpoint component for
Data Exchange Framework, those settings are added to the endpoint.

A *plugin* is used to store the settings. The *converter* instantiates 
the plugin, sets the values on the plugin and then adds the plugin to
the endpoint.

Before any of that can happen, a plugin is needed.

1. In Visual Studio, add the following class:

    .. code-block:: c#

        namespace Examples.FileSystem.Plugins
        {
            public class TextFileSettings : Sitecore.DataExchange.IPlugin
            {
                public TextFileSettings()
                {
                }
                public bool ColumnHeadersInFirstLine { get; set; }
                public string ColumnSeparator { get; set; }
                public string Path { get; set; }
            }
        }

2. Add the following class:

    .. code-block:: c#

        using Sitecore.DataExchange.Models;
        using Examples.FileSystem.Plugins;
        using System;

        namespace Examples.FileSystem
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

        This extension method makes it easier to access the plugin  
        when it is needed. 
        
        Providing extension methods to access a plugin is a best 
        practice to consider when implementing a provider for 
        Data Exchange Framework.
