CRM Contacts
==========================================

This *queue processor* is reads CRM contacts from the queue and writes 
those contacts to CRM using the ExecuteMultipleRequest_ API.

.. _ExecuteMultipleRequest: https://msdn.microsoft.com/en-us/library/jj863631.aspx

+-----------------+------------------------------------------------------------------------+
| Template name   | **Queue Processor for CRM Contacts**                                   |
+-----------------+------------------------------------------------------------------------+
| Base template   | :doc:`../../../framework/queues/queue-processors/base-queue-processor` |
+-----------------+------------------------------------------------------------------------+

This queue processor handles the following types of queue entries:

    * ``Microsoft.Xrm.Sdk.Entity``