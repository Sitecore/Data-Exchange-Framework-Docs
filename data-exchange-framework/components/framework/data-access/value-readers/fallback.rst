Fallback
==========================================

This *value reader* is used to specify additional value readers 
that are used in the event that no value is read.

.. tip:: 

    This value reader is usually used with a :doc:`sequential` value reader. 

+-----------------+-----------------------------------------------------------+
| Template name   | **Fallback Value Reader**                                 |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-reader`                                  |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Readers``                                   | | The value readers that are used until a value is read.  | 
|                                               | |                                                         |
|                                               | | In order for the fallback value reader to stop looping  |
|                                               | | through the readers, a non-null value must be read,     |
|                                               | | or, if a value that is read is a value-type, a non-     |
|                                               | | default value must be read.                             |
+-----------------------------------------------+-----------------------------------------------------------+

.. tip:: 

    This value reader is used to ensure an email address is available 
    when pushing xDB contact data to Dynamics CRM.

    The synchronization process wants to use the same email address
    that was read from CRM in order to find the CRM contact to update.
    But this only works when the xDB has already been synchronized 
    with CRM. The only way xDB could know the CRM email address is 
    if xDB is already storing the CRM email address.

    If the xDB contact does not have a CRM email address, another 
    email address should be used. This is where the fallback value
    reader comes in. If no CRM email is read on the xDB contact,
    a different email address is read from the xDB contact.
