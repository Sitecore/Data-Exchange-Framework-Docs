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

+-------------------------------------------------------+---------------------------------------------------+
| Field                                                 | Description                                       |
+=======================================================+===================================================+
| ``Queue Processor``                                   | | The queue processor to use.                     |
+-------------------------------------------------------+---------------------------------------------------+
| ``Make Processed Entries Available As Iterable Data`` | | If checked, processed entries are made          |
|                                                       | | available to subsequent pipeline steps.         |
+-------------------------------------------------------+---------------------------------------------------+
| ``Post Process Pipeline Batches``                     | | The pipeline batches to run after all of the    |
|                                                       | | queue entries have been processed.              |
+-------------------------------------------------------+---------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| ``IterableDataSettings``          | | Provides access to the collection of data objects that were         |
|                                   | | processed by the queue processor.                                   |
|                                   | |                                                                     |
|                                   | | This plugin is created and added to the current pipeline context    |
|                                   | | as the queue entries are processed, provided the field              |
|                                   | | ``Make Processed Entries Available As Iterable Data`` is enabled.   |
|                                   | | This makes the processed data object available to subsequent        |
|                                   | | pipeline steps.                                                     |
+-----------------------------------+-----------------------------------------------------------------------+
| ``ParentPipelineContextSettings`` | | Provides access to the current pipeline context to the              | 
|                                   | | pipeline batches specified in the ``Post-process pipeline batches`` |
|                                   | | field.                                                              | 
|                                   | |                                                                     |
|                                   | | This pipeline step creates this plugin and adds it to the new       |
|                                   | | pipeline context that is passed to the specified pipeline           |
|                                   | | batches.                                                            |
+-----------------------------------+-----------------------------------------------------------------------+
