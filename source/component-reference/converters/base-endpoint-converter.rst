Base Endpoint Converter
===================================================
This class provides methods to simplify reading values
from Sitecore items that are set on plugins that are
added to an endpoint for Data Exchange Framework.

.. |type| replace:: ``Sitecore.DataExchange.Converters.Endpoints.BaseEndpointConverter, Sitecore.DataExchange``

+---------------------------+---------------------------------------------------------------------+
| Type                      | |type|                                                              |
+---------------------------+---------------------------------------------------------------------+

The class always adds the plugin ``SitecoreItemSettings``. 
This plugin stores the item id for Sitecore item that 
represents the endpoint.

Additional plugins are added to the endpoint by overriding 
the method ``AddPlugins(ItemModel, Endpoint)``.
