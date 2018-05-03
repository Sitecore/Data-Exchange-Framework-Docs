Object Field Value Accessor
===================================================
This value accessor provides the ability to read 
and write a field a Salesforce object.

.. |object-type-label| replace:: Expected source/target object type
.. |object-type| replace:: ``System.Collections.Generic.IDictionary<string, object>``
.. |template-location| replace:: **Data Exchange > Providers > Salesforce > Data Access > Value Accessors > Salesforce Object Field Value Accessor**

+---------------------------+---------------------------------------------------------------------+
| |object-type-label|       | |object-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |field-name| replace:: Name of the field from a Salesforce object whose value can be read and written.
.. |field-name-for-select| replace:: If the name of the field used in the SOQL select statement (used to read data from Salesforce) does not match the name of the field on the object returned by the statement, this field is used to specify the field name for the SOQL statement.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Field Name                | |field-name|                                                        |
+---------------------------+---------------------------------------------------------------------+
| Field Name for Select     | |field-name-for-select|                                             |
+---------------------------+---------------------------------------------------------------------+
