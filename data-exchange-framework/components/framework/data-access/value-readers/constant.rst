Constant
==========================================

This *value reader* is used to read a constant string value.

+-----------------+-----------------------------------------------------------+
| Template name   | **Constant Value Reader**                                 |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-reader`                                  |
+-----------------+-----------------------------------------------------------+

+--------------------------------+--------------------------------------------------------------------------+
| Field                          | Description                                                              |
+================================+==========================================================================+
| ``Value``                      | | The value that is returned when the value reader is used.              |
+--------------------------------+--------------------------------------------------------------------------+
| ``Value type``                 | | The value is converted to this type before being returned.             |
|                                | |                                                                        |
|                                | | This property is used when the value represents a number or a          |
|                                | | character.                                                             |
|                                | |                                                                        |
|                                | | The default value is ``System.Object``, which means the value          |
|                                | | is not converted.                                                      |
+--------------------------------+--------------------------------------------------------------------------+

.. tip:: 

    This value reader is used to set the key for various dictionary
    properties on the xDB contact facet that is populated with CRM
    data, such as email address, telephone number and address.
