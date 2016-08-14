Architecture
=======================================

This section provides an overview of the architecture used by
Data Exchange Framework and its remote SDK.

Configuration Using Sitecore Items
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All Data Exchange Framework components are configured using Sitecore 
items. There are several advantages to this approach:

    * The Sitecore client provides a rich user-interface for creating
      and editing Sitecore items. Sitecore field editors offer type-specific
      options. Relationships between components can be easily modeled.
    * Sitecore items can be accessed directly on the Sitecore server or
      via a web service.

Accessing Sitecore Items Using Item Model Repository
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When accessing the Sitecore items that represent Data Exchange Framework 
components, an *item model repository* is used. This is a component that
provides a layer of abstraction between the Sitecore API and the framework.

    .. hint:: 
    
        Sitecore provides several APIs that can be used to access Sitecore
        items. The Data Exchange Framework's item model repository API
        provides a single, simplified API for accessing Sitecore items
        so that a developer does not need to be a Sitecore expert in 
        order to write framework components.

Converting Sitecore Items Into Framework Components
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Sitecore items used for configuration must be converted into  
Data Exchange objects. This is handled by *converters*.  Data 
Exchange Framework provides APIs that hide most of the work 
involved in converting Sitecore items into framework objects.

Remote SDK Limitations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In order for a Data Exchange Framework component to work outside of the
Sitecore server, the component must not have any dependencies on APIs
that are only available on the Sitecore server.

    .. hint:: 
    
        This is the reason why the item model repository API does not 
        read items using the ``Sitecore.Data.Items.Item`` type. 

The following is a list of some of the things you cannot do in your 
component if you want to be able to use your component with the remote
SDK:

    * Run Sitecore pipelines (Data Exchange Framework provides its own
      pipeline implementation that can be used instead)
    * Reading anything from Sitecore configuration files
    * Using any type defined in Sitecore assemblies 
      (**Sitecore.Services.Core.dll** is the one exception) 
