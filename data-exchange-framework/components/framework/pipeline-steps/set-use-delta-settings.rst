Set Use Delta Settings
=============================

The purpose of this *pipeline step* is to determine a date range by
reading a date/time from the *pipeline context* and then converting
it into a date range.    

The most common use of this pipeline step is to determine a date range
for reading data in order to only read data that has changed within
the date range (such as within the last 30 days).

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Set Use Delta Settings Pipeline Step**                              |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`base-pipeline-step`                                             |
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
