Description to Code Value Reader
===================================================
This value reader is used to convert a string into 
a specified integer value.

The mapping of descriptions to values is defined in 
an item called a code definition set. A code definition
set is a collection of code definition items. Each
code definition item has a value (stored in a field)
and a description (stored in the item name).

.. |source-type-label| replace:: Expected source object type
.. |source-type| replace:: ``System.String``
.. |template-location| replace:: **Data Exchange > Framework > Data Access > Value Readers > Description to Code Reader**

+---------------------------+---------------------------------------------------------------------+
| |source-type-label|       | |source-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |comment| replace:: The code definition set where the mapping of the description to a value is defined\ :sup:`1`.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Code Definition Set       | |comment|                                                           |
+---------------------------+---------------------------------------------------------------------+

:sup:`1` Code definition sets are defined under a tenant at **Tenant Settings > Common > Code Definition Sets**
