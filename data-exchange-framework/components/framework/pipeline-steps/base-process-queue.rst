Base Process Queue
=============================

This template is the base template for any *pipeline step* that processes the items  
in a *work queue* using a *queue processor*. After the queue entries are processed,
additional *pipeline batches* are run (if specified).

.. include:: ../../../../common/base-template-always-inherit-notice.txt

Template Information
-----------------------------

+--------------------------------+--------------------------------------------------------------------------+
| Template name                  | **Base Process Queue Pipeline Step**                                     |
+--------------------------------+--------------------------------------------------------------------------+
| Base template                  | :doc:`base-pipeline-step`                                                |
+--------------------------------+--------------------------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Queue processor``                           | | The queue processor to use.                             |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Post-process pipeline batches``             | | The pipeline batches to run after all of the queue      |
|                                               | | entries have been processed.                            |
+-----------------------------------------------+-----------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| ``ParentPipelineContextSettings`` | | Provides access to the current pipeline context to the              | 
|                                   | | pipeline batches specified in the ``Post-process pipeline batches`` |
|                                   | | field.                                                              | 
|                                   | |                                                                     |
|                                   | | This pipeline step creates this plugin and adds it to the new       |
|                                   | | pipeline context that is passed to the specified pipeline           |
|                                   | | batches.                                                            |
+-----------------------------------+-----------------------------------------------------------------------+
