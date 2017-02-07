Base Queue Processor
==========================================

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
|                                               | | status values are processed.                            |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Remove Unprocessed Entries``                | | When the processor is finished running, any unprocessed |
|                                               | | entries are removed from the queue if this field is     |
|                                               | | ticked.                                                 |
+-----------------------------------------------+-----------------------------------------------------------+
