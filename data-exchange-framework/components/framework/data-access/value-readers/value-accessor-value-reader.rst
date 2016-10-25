Value Accessor Value Reader
==========================================

This *value reader* uses the value reader assigned to a *value accessor*.

This value reader allows you to reuse existing configuration.

+-----------------+-----------------------------------------------------------+
| Template name   | **Value Accessor Value Reader**                           |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-reader`                                  |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Value Accessor``                            | The value accessor whose value reader is used.            |
+-----------------------------------------------+-----------------------------------------------------------+

.. tip:: 

    This value reader is used by the :doc:`fallback` value reader, which 
    ensures an email address is available on the xDB contact when CRM
    is updated using data from xDB.

    The fallback value reader uses value readers, but the ability to access
    email addresses on the xDB contact uses value accessors. Rather than
    require new value reader be defined that replicate the functionality
    already implemented in the value accessors, this value reader is used
    to get a reference to the value reader that is assigned to the value 
    accessor.