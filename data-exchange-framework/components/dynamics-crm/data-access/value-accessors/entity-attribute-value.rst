Entity Attribute Value
==========================================

This *value accessor* is used to access an attribute value on a Dynamics CRM entity.

+-----------------------------------+---------------------------------------------------------------------------------+
| Template name                     | **Entity Attribute Value Accessor**                                             |
+-----------------------------------+---------------------------------------------------------------------------------+
| Base template                     | :doc:`../../../framework/data-access/value-accessors/base-value-accessor`       |
+-----------------------------------+---------------------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Attribute Name``                | | Name of the attribute on a CRM entity whose value is accessed.      |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Use Value Property``            | | The object that is read using the attribute name is an object with  |
|                                   | | a property ``Property``. The value of this property should be used. |
|                                   | |                                                                     |
|                                   | | Whether this setting is applicable or not depends on the *entity*   |
|                                   | | *repository* used to read the entity.                               |
|                                   | |                                                                     |
|                                   | | This setting is used to determine the appropriate value reader.     | 
+-----------------------------------+-----------------------------------------------------------------------+
