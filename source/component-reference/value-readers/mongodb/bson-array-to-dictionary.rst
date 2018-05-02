BSON Array To Dictionary Value Reader
===================================================
This value reader is used to create a new dictionary
and to read members of an array into the dictionary. 
Properties on each member of the array are used to 
represent the keys and values for the dictionary.

.. |source-type-label| replace:: Expected source object type
.. |source-type| replace:: ``MongoDB.Bson.BsonArray``
.. |template-location| replace:: **Data Exchange > Providers > MongoDB > Data Access > Value Readers > BSON Array To Dictionary Value Reader**

+---------------------------+---------------------------------------------------------------------+
| |source-type-label|       | |source-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |key| replace:: Name of the property on the member of the array to use as the key value when an entry is added to the dictionary.
.. |value| replace:: Name of the property on the member of the array to use as the value when an entry is added to the dictionary.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Key Field Name            | |key|                                                               |
+---------------------------+---------------------------------------------------------------------+
| Value Field Name          | |value|                                                             |
+---------------------------+---------------------------------------------------------------------+
