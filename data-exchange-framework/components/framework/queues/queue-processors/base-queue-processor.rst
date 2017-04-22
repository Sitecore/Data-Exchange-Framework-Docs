Base Queue Processor
==========================================

.. |status| replace:: :doc:`/components/framework/queues/queue-entry-status`

This template is the base template for all *queue processors*.

.. include:: ../../../../../common/base-template-always-inherit-notice.txt

+-----------------+-----------------------------------------------------------+
| Template name   | **Base Queue Processor**                                  |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Process Entries``                           | | Only entries that match at least one of the selected    |
|                                               | | |status| values are processed.                          |
|                                               | |                                                         |
|                                               | | Processed entries are automatically removed from the    |
|                                               | | queue.                                                  |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Remove Entries``                            | | When the processor is finished running, any entries     |
|                                               | | that match at least one of the selected |status| values |
|                                               | | will be removed from the queue.                         |
+-----------------------------------------------+-----------------------------------------------------------+
