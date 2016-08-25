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
| ``Contact facet name``            | | Name of the contact facet to access.                                |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Property name``                 | | Name of the property on the contact facet.                          |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Value appender type``           | | Type that is able to add a value to the collection.                 | 
|                                   | |                                                                     |
|                                   | | In most cases you will not need to change this value.               |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Do not use value appender``     | | Specifies whether or not the Value Appender is used.                |
|                                   | |                                                                     |
|                                   | | Enable this value if you want to overwrite the value on the         |
|                                   | | contact facet. An example is when you want to reset the             |
|                                   | | value.                                                              |
|                                   | |                                                                     |
|                                   | | Disable this value if you want to use the value appender.           |
|                                   | | This will allow you to add values to the collection without         |
|                                   | | losing values that already exist in the collection.                 |
+-----------------------------------+-----------------------------------------------------------------------+
