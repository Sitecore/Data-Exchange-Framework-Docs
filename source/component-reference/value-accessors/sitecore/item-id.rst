Item Id Value Accessor
===================================================
This value accessor provides the ability to read 
the id of the specified Sitecore item.

.. |object-type-label| replace:: Expected source object type
.. |object-type| replace:: ``Sitecore.Services.Core.Model.ItemModel``
.. |template-location| replace:: **Data Exchange > Providers > Sitecore > Data Access > Value Accessors > Sitecore Item Field Value Accessor**

+---------------------------+---------------------------------------------------------------------+
| |object-type-label|       | |object-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

.. note::

    This value accessor is read-only because the value 
    it accesses is read-only. It does not provide the 
    ability to write values because the id on a Sitecore 
    item cannot be changed.

Template Fields
---------------------------------------------------

.. |item| replace:: The Sitecore item whose id can be read.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Item                      | |item|                                                              |
+---------------------------+---------------------------------------------------------------------+
