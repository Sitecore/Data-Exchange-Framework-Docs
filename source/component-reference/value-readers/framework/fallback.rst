Fallback Value Reader
===================================================
This value reader runs a series of other value readers
until a non-null, non-default value is read, or the 
last value reader in the series is used.

This value reader is used in cases where you want to 
avoid having no value read.

.. |source-type-label| replace:: Expected source object type
.. |source-type| replace:: ``System.Object``
.. |template-location| replace:: **Data Exchange > Framework > Data Access > Value Readers > Fallback Value Reader**

+---------------------------+---------------------------------------------------------------------+
| |source-type-label|       | |source-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |readers| replace:: The value readers that are run in the specified order.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Readers                   | |readers|                                                           |
+---------------------------+---------------------------------------------------------------------+
