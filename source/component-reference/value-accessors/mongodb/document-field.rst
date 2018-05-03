Document Field Value Accessor
===================================================
This value accessor provides the ability to read 
a value from a field on a MongoDB document.

.. |object-type-label| replace:: Expected source/target object type
.. |object-type| replace:: ``MongoDB.Bson.BsonElement`` or ``MongoDB.Bson.BsonDocument``
.. |template-location| replace:: **Data Exchange > Providers > MongoDB > Data Access > Value Accessors > MongoDB Document Field Value Accessor**

+---------------------------+---------------------------------------------------------------------+
| |object-type-label|       | |object-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

.. note::

    This value accessor is read-only.

Template Fields
---------------------------------------------------

.. |field-name| replace:: The name of the field whose value is read.
.. |value-reader| replace:: The component used to convert the BSON value to a value that can be used outside of MongoDB.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Field Name                | |field-name|                                                        |
+---------------------------+---------------------------------------------------------------------+
| BSON Field Value Reader   | |value-reader|                                                      |
+---------------------------+---------------------------------------------------------------------+
