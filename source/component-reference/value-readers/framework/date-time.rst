Date Time Value Reader
===================================================
This value reader returns a date/time object. It is 
used to ensure a value read from a source object is 
a date/time object.

.. |source-type-label| replace:: Expected source object type
.. |source-type| replace:: ``System.DateTime`` or ``System.String``
.. |template-location| replace:: **Data Exchange > Framework > Data Access > Value Readers > Date Time Value Reader**

+---------------------------+---------------------------------------------------------------------+
| |source-type-label|       | |source-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |string-format| replace:: If a value is specified and the source object is a string, the value reader expects the source object to be a date in the specified format. If the source object is not a string, this value is not used. For details on the supported options, see ``Guid.ToString(String)``.
.. |read-date-only| replace:: If ticked, the date/time object includes only the date. If not ticked, the date-time object includes both the date and the time.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| String Format             | |string-format|                                                     |
+---------------------------+---------------------------------------------------------------------+
| Read Date Only            | |read-date-only|                                                    |
+---------------------------+---------------------------------------------------------------------+
