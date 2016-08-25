Apply Mapping
=============================

This *pipeline step* is used to apply a *value mapping set* so that 
values from the *source object* are written to the *target object*.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Apply Mapping Pipeline Step**                                       |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`base-pipeline-step`                                             |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Mapping set``                   | The value mapping set to apply.                                       |
+-----------------------------------+-----------------------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``SynchronizationSettings``       | | Provides access to the source object and the target object.         |
|                                   | |                                                                     |
|                                   | | If this plugin is not set on the pipeline context prior to this     | 
|                                   | | pipeline step running, the pipeline step will abort. This is not a  |
|                                   | | *critical error*.                                                   |
|                                   | |                                                                     |
|                                   | | If either the source object or the target object is not set prior   |
|                                   | | to this pipeline step running, the pipeline step will abort. This   |
|                                   | | is not a *critical error*.                                          |
+-----------------------------------+-----------------------------------------------------------------------+

.. hint:: 

    If a *value mapping* fails, an error is written to the log. Increase the log level to 
    debug to get a list of the specific value mappings that failed.
