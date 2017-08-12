Run Bulk Salesforce Object Update from Queue
=================================================

.. |queue| replace:: :doc:`../queues/queue-processors/salesforce-contacts`
.. |endpoint| replace:: :doc:`../endpoints/salesforce-object`

This *pipeline step* is used to run the Salesforce bulk object update process using the 
Salesforce objects in a *work queue*.

A |queue| *queue processor* must be specified for this pipeline step. 

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Run Bulk Contact Update from Queue Pipeline Step**                  |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-process-queue-from-endpoint`|
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------------+-----------------------------------------------------------------------+
| Field                                   | Description                                                           |
+=========================================+=======================================================================+
| ``Batch Size``                          | | Determines the maximum number of Salesforce objects that            |
|                                         | | will be updated at a time.                                          |
|                                         | |                                                                     |
|                                         | | For example, if 200 Salesforce contacts need to be updated          |
|                                         | | and the batch size is 75, 3 separate commands will be sent          |
|                                         | | to Salesforce in order for all 200 objects to be updated.           |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Data Context``                        | | The *data context* value used to during the bulk contact            |       
|                                         | | update process.                                                     |
|                                         | |                                                                     |
|                                         | | The default value is ``DataExchange``. This value must match the    |
|                                         | | value in the ``updateFields`` pipeline for the xDB bulk contact     |
|                                         | | API. In most cases you will not need to change this value.          |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Queue Endpoint``                      | | The endpoint for the queue from which Salesforce objects            |
|                                         | | are read.                                                           |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Endpoint To``                         | | The |endpoint| endpoint that represents where the bulk              | 
|                                         | | object update command is submitted to.                              |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Salesforce Object Name``              | | Objects with this name are processed.                               |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Salesforce Object Lookup Field Name`` | | The value read by Identifier Value Accessor is matched to a         |
|                                         | | Salesforce object using the value in this field on the              |
|                                         | | Salesforce object.                                                  |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Max Retries``                         | | When the queue processor interacts with Salesforce, a               |
|                                         | | failure may occur. This value tells the processor to                |
|                                         | | retry up to a certain number of times before returning              |
|                                         | | an error.                                                           |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Retry Interval``                      | | This value tells the queue processor that is able retry an          |
|                                         | | operation to wait a certain amount of time before retrying          |
|                                         | | the operation.                                                      |
+-----------------------------------------+-----------------------------------------------------------------------+


