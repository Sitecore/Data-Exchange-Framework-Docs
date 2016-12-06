Contact Facet Property (Collection)
==========================================

This *value accessor* is used for properties that are collections.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **xDB Contact Facet Collection Property Value Accessor**              |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`contact-facet-property`                                         |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Contact Facet Name``            | | Name of the contact facet to access.                                |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Property Name``                 | | Name of the property on the contact facet.                          |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Value Appender Type``           | | The .NET type that is able to add a value to the collection.        |
|                                   | | Specifically, a type that implements                                |
|                                   | | ``Sitecore.DataExchange.DataAccess.IValueAppender``.                |
|                                   | |                                                                     |
|                                   | | In most cases you will not need to change this value.               |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Do Not Use Value Appender``     | | Specifies whether or not the *value appender* is used.              |
|                                   | |                                                                     |
|                                   | | Enable this value if you want to overwrite the value on the         |
|                                   | | contact facet. An example is when you want to reset the             |
|                                   | | value.                                                              |
|                                   | |                                                                     |
|                                   | | Disable this value if you want to use the value appender.           |
|                                   | | This will allow you to add values to the collection without         |
|                                   | | losing values that already exist in the collection.                 |
+-----------------------------------+-----------------------------------------------------------------------+
