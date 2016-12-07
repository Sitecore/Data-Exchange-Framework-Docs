.. |read-entities| replace:: :doc:`read-entities`

Set Use Delta Settings
=============================

This *pipeline step* is used to set the values that are used by the 
pipeline step |read-entities| to build a filter so that only entities
that have changed within a certain date range are read from CRM.

The purpose of this pipeline step is to determine the date range by
reading a date/time from the *pipeline context* and then converting
it into a date range.    

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Set Use Delta Settings Pipeline Step**                              |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Context Value Reader``          | | The *value reader* responsible for reading a date/time from the     |
|                                   | | pipeline context.                                                   |
|                                   | |                                                                     |
|                                   | | An example is a value reader that reads when the *pipeline batch*   |
|                                   | | was last run.                                                       |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Operator``                      | | The value that determines the kind of date range to create.         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Offset``                        | | An integer value that determines how the date range is created.     |
|                                   | |                                                                     |
|                                   | | A negative integer means to use a date in the past.                 |
|                                   | |                                                                     |
|                                   | | A positive integer means to use a date in the future.               |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Unit of Time``                  | | The value that specifies the unit for the **Offset** value.         |
+-----------------------------------+-----------------------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``DateRangeSettings``             | | Subsequent pipeline steps use this plugin to access the date        |
|                                   | | range created by this pipeline step.                                |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
