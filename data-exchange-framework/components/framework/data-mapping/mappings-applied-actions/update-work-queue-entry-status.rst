Update Work Queue Entry Status
==========================================

.. |endpoint| replace:: :doc:`/components/framework/endpoints/queue`

This *mappings applied action* is used to update the status on an entry in a work queue.

+-----------------+-----------------------------------------------------------+
| Template name   | **Update Work Queue Entry Status Action**                 |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-mappings-applied-action`                       |
+-----------------+-----------------------------------------------------------+

+-------------------------------------+-----------------------------------------------------------+
| Field                               | Description                                               |
+=====================================+===========================================================+
| ``Queue Endpoint``                  | The |endpoint| endpoint that provides access to the queue.|  
+-------------------------------------+-----------------------------------------------------------+
| ``Work Queue Entry Status``         | The status to which the queue entry is set.               |
+-------------------------------------+-----------------------------------------------------------+
