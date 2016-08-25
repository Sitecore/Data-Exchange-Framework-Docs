Iterate Data and Run Pipelines
==========================================

This *pipeline step* iterates a collection of objects and runs a set of 
*pipelines*, using the data object as the *source object*.

Template Information
-----------------------------

+--------------------------------+--------------------------------------------------------------------------+
| Template name                  | **Iterate Data and Run Pipelines Pipeline Step**                         |
+--------------------------------+--------------------------------------------------------------------------+
| Base template                  | :doc:`base-pipeline-step`                                                |
+--------------------------------+--------------------------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Pipelines``                                 | The pipelines to run.                                     |
+-----------------------------------------------+-----------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``IterableDataSettings``          | | Provides access to the collection of data objects that are passed   |
|                                   | | to the pipelines.                                                   |
|                                   | |                                                                     |
|                                   | | If this plugin is not set on the pipeline context prior to this     | 
|                                   | | pipeline step running, the pipeline step will abort. This is not a  |
|                                   | | *critical error*.                                                   |
+-----------------------------------+-----------------------------------------------------------------------+
| ``SynchronizationSettings``       | | When the pipeline step runs, it loops through the data objects.     |
|                                   | | For each data object, a new pipeline context is created. This       |
|                                   | | pipeline context is passed to each of the pipelines specified in    |
|                                   | | the ``Pipelines`` field.                                            |
|                                   | |                                                                     |
|                                   | | The data object is set as the source object in this plugin.         |
|                                   | |                                                                     |
|                                   | | This pipeline step creates this plugin and adds it to the new       |
|                                   | | pipeline context that is passed to the specified pipelines.         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``ParentPipelineContextSettings`` | | Provides access to the current pipeline context to the pipelines    | 
|                                   | | specified in the ``Pipelines`` field.                               | 
|                                   | |                                                                     |
|                                   | | This pipeline step creates this plugin and adds it to the new       |
|                                   | | pipeline context that is passed to the specified pipelines.         |
+-----------------------------------+-----------------------------------------------------------------------+
