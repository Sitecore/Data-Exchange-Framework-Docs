Constructor Value Reader
===================================================
This value reader is used to call a constructor and 
return the object that is created. 

Which constructor is called depends on the source object
that is passed to the value reader:

    * If the source object is null, the default constructor is called.
    * If the source object is not a collection, the source object is passed as a parameter to the constructor.
    * If the source object is a collection, each member of the collection is passed as a separate parameter to the constructor.

.. |source-type-label| replace:: Expected source object type
.. |source-type| replace:: ``System.Object``
.. |template-location| replace:: **Data Exchange > Framework > Data Access > Value Readers > Constructor Value Reader**

+---------------------------+---------------------------------------------------------------------+
| |source-type-label|       | |source-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |type| replace:: Type whose constructor is called.
.. |parameters-label| replace:: Do Not Use Source For Constructor Parameters
.. |parameters| replace:: If ticked, no parameters will be passed to the constructor, even if the source object is not null.
.. |parameter-types| replace:: If the type has generic parameters, this field is used to specify the generic parameter types. In order to specify multiple types, separate the type names with a line break.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Type                      | |type|                                                              |
+---------------------------+---------------------------------------------------------------------+
| |parameters-label|        | |parameters|                                                        |
+---------------------------+---------------------------------------------------------------------+
| Generic Parameter Types   | |parameter-types|                                                   |
+---------------------------+---------------------------------------------------------------------+


