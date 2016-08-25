xDB Contacts
==========================================

This *queue processor* is reads xDB contacts from the queue and writes 
those contacts to xDB using the bulk contact update API.

+-----------------+---------------------------------------------------------------------+
| Template name   | **Queue Processor for xDB Contact**                                 |
+-----------------+---------------------------------------------------------------------+
| Base template   | :doc:`../../framework/queue-processors/base-queue-processor`        |
+-----------------+---------------------------------------------------------------------+

This queue processor handles the following types of queue entries:

    * ``Sitecore.Analytics.Model.Entities.IContactTemplate``