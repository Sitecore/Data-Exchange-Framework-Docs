Run Bulk CRM Entity Update from Queue
=================================================

.. |queue| replace:: :doc:`../queues/queue-processors/crm-contacts`
.. |endpoint| replace:: :doc:`../endpoints/crm-entities`

This *pipeline step* is used to run the CRM bulk entity update process using the 
CRM entities in a *work queue*.

A |queue| *queue processor* must be specified for this pipeline step. 

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Run Bulk Contact Update from Queue Pipeline Step**                  |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-process-queue-from-endpoint`|
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Batch Size``                    | | Determines the maximum number of CRM entities that will be          |
|                                   | | updated at a time.                                                  |
|                                   | |                                                                     |
|                                   | | For example, if 200 CRM contacts need to be updated and the         |
|                                   | | batch size is 75, 3 separate commands will be sent to CRM in        |
|                                   | | order for all 200 entities to be updated.                           |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Data Context``                  | | The *data context* value used to during the bulk contact update     |       
|                                   | | process.                                                            |
|                                   | |                                                                     |
|                                   | | The default value is ``DataExchange``. This value must match the    |
|                                   | | value in the ``updateFields`` pipeline for the xDB bulk contact     |
|                                   | | API. In most cases you will not need to change this value.          |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Queue Endpoint``                | | The endpoint for the queue from which CRM entities are read.        |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Endpoint To``                   | | The |endpoint| endpoint that represents where the bulk entity       | 
|                                   | | bulk entity update command is submitted to.                         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Entity Name``                   | | Entities with this name are processed.                              |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Max Retries``                   | | When the queue processor interacts with the entity repository set,  |
|                                   | | a failure may occur. This value tells the processor to retry up to  |
|                                   | | a certain number of times before returning an error.                |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Retry Interval``                | | This value tells the queue processor that is able retry an          |
|                                   | | operation to wait a certain amount of time before retrying the      |
|                                   | | operation.                                                          |
+-----------------------------------+-----------------------------------------------------------------------+


