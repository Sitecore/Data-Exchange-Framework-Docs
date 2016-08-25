Base Process Queue from Endpoint
=================================================

.. |endpoint| replace:: :doc:`/components/framework/endpoints/queue`

This template is the base template for any *pipeline step* that processes the items  
in a *work queue* and accesses the queue from a |endpoint| *endpoint*.


.. include:: ../../../../common/base-template-always-inherit-notice.txt

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Base Process Queue from Endpoint Pipeline Step**                    |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`base-process-queue`                                             |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Queue endpoint``                | The |endpoint| endpoint that provides access to the queue.            |
+-----------------------------------+-----------------------------------------------------------------------+
