Collection Count Apply Mapping Rule
===================================================
This rule is used to ensure a value is a collection 
with a number of members within a specific range.

.. |value-type-label| replace:: Expected type of the value being written to the target object
.. |value-type| replace:: ``System.Collections.ICollection``
.. |template-location| replace:: **Data Exchange > Apply Mapping Rules > Collection Count Mapping Rule**

+---------------------------+---------------------------------------------------------------------+
| |value-type-label|        | |value-type|                                                        |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |max| replace:: The collection may not contain more than this many members. The default value is -1, which means that the collection may contain an unlimited number of members.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Minimum Count             | The collection must contain at least this many members.             |
+---------------------------+---------------------------------------------------------------------+
| Maximum Count             | |max|                                                               |
+---------------------------+---------------------------------------------------------------------+
