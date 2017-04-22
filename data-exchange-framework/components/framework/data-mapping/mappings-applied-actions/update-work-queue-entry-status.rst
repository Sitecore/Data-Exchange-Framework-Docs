Update Work Queue Entry Status
==========================================

.. |endpoint| replace:: :doc:`/components/framework/endpoints/queue`
.. |status| replace:: :doc:`/components/framework/queues/queue-entry-status`

This *mappings applied action* is used to update the status on an entry in a work queue.

+-----------------+-----------------------------------------------------------+
| Template name   | **Update Work Queue Entry Status Action**                 |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-mappings-applied-action`                       |
+-----------------+-----------------------------------------------------------+

+---------------------------------------------------+---------------------------------------------+
| Field                                             | Description                                 |
+===================================================+=============================================+
| ``Queue Endpoint``                                | | The |endpoint| endpoint that provides     |
|                                                   | | access to the queue.                      |  
+---------------------------------------------------+---------------------------------------------+
| ``Work Queue Entry Status``                       | | The |status| the queue entry is set to.   |
+---------------------------------------------------+---------------------------------------------+
| ``Source Object Location For Key Value Accessor`` | | Location of the object whose value is     |
|                                                   | | read in oprder to find the appropriate    |
|                                                   | | work queue entry.                         |
+---------------------------------------------------+---------------------------------------------+
| ``Key Value Accessor``                            | | Component whose value reader is used to   |
|                                                   | | read the value from the object that is    |
|                                                   | | used to locate the appropriate work queue |
|                                                   | | entry.                                    |
+---------------------------------------------------+---------------------------------------------+
