Run Bulk Campaign Update from Queue
=================================================

.. |queue| replace:: :doc:`../queues/queue-processors/marketing-campaigns`
.. |endpoint| replace:: :doc:`../endpoints/marketing-campaign-repo`

This *pipeline step* is used to run the marketing campaign update process using the 
marketing campaigns in a *work queue*.

A |queue| *queue processor* must be specified for this pipeline step. 

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Run Bulk Campaign Update from Queue Pipeline Step**                 |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-process-queue-from-endpoint`|
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Disable Indexing``              | | Marketing campaigns are represented in Sitecore using items.        |
|                                   | | When an item is saved, Sitecore automatically reindexes the         |
|                                   | | item. When a large number of items are being saved, this can        |
|                                   | | have a negative impact on Sitecore server performance.              |
|                                   | |                                                                     |
|                                   | | This option ensures indexing is temporarily for marketing           |
|                                   | | campaigns until all of the campaigns in the queue have been saved.  |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Endpoint To``                   | | The |endpoint| endpoint that represents where the                   | 
|                                   | | bulk campaign update command is submitted to.                       |
+-----------------------------------+-----------------------------------------------------------------------+
