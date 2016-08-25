Run Bulk Contact Update from Queue
=================================================

.. |queue| replace:: :doc:`../queue-processors/xdb-contacts`
.. |endpoint| replace:: :doc:`../endpoints/local-xdb-contacts`

This *pipeline step* is used to run the xDB bulk contact update process using the 
xDB contacts in a *work queue*.

A |queue| *queue processor* must be specified for this pipeline step. 

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Run Bulk Contact Update from Queue Pipeline Step**                  |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-process-queue-from-endpoint`|
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------------+-----------------------------------------------------------------+
| Field                                   | Description                                                     |
+=========================================+=================================================================+
| ``Data context``                        | | The *data context* value used to during the bulk              |       
|                                         | | contact update process.                                       |
|                                         | |                                                               |
|                                         | | The default value is ``DataExchange``. This value             |
|                                         | | must match the value in the ``updateFields``                  |
|                                         | | pipeline for the xDB bulk contact API. In most                | 
|                                         | | cases you will not need to change this value.                 |
+-----------------------------------------+-----------------------------------------------------------------+
| ``Endpoint for xDB contact repository`` | | The |endpoint| endpoint that represents where the             | 
|                                         | | bulk contact update command is submitted to.                  |
+-----------------------------------------+-----------------------------------------------------------------+
