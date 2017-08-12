Salesforce Contacts
==========================================

This *queue processor* is reads Salesforce contacts from the queue and writes 
those contacts to Salesforce using the Bulk_ API.

.. _Bulk: https://developer.salesforce.com/page/Bulk_API

+-----------------+------------------------------------------------------------------------+
| Template name   | **Queue Processor for Salesforce Contacts**                            |
+-----------------+------------------------------------------------------------------------+
| Base template   | :doc:`../../../framework/queues/queue-processors/base-queue-processor` |
+-----------------+------------------------------------------------------------------------+

This queue processor handles the following types of queue entries:

    * ``Salesforce.Common.Models.Xml.SObject``