Plugin
=======================================

A *plugin* is a component that provides settings to a Data Exchange 
Framework component.

For example, consider an *endpoint* that represents a connection to
a CRM. Settings must be configured on the endpoint in order to 
identify the CRM. In Data Exchange Framework, you do not extend the
endpoint type. Instead, you use a plugin.

A plugin represents the settings that are needed to identify the CRM.
The plugin is then added to the endpoint.

.. hint:: 

    A *converter* is responsible for instantiating the appropriate 
    plugins and adding those plugins to any components it creates. 