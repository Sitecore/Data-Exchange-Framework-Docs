Preferred Email
==========================================

This *value reader* is used to read the preferred email address for 
an xDB contact.

+-------------------------+---------------------------------------------------------------------------------+
| Template name           | **Preferred Email Address Reader**                                              |
+-------------------------+---------------------------------------------------------------------------------+
| Base template           | :doc:`../../../framework/data-access/value-readers/base-value-reader`           |
+-------------------------+---------------------------------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Contact facet name``                        | The value that is returned when the value reader is used. |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Property name on contact facet``            | The value that is returned when the value reader is used. |
+-----------------------------------------------+-----------------------------------------------------------+

.. tip:: 

    This value reader is used by the :doc:`../../../framework/data-access/value-readers/fallback` value reader 
    that ensures an email address is available on the xDB contact when CRM
    is updated using data from xDB.

    If the CRM email address is not set on the xDB contact, this value
    reader is used to read the preferred email address from the xDB
    contact.
