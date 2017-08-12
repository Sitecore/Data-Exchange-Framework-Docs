Read Salesforce Objects
=============================

This *pipeline step* is used to read object from Salesforce.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Read CRM Entities Pipeline Step**                                   |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

.. |ep| replace:: :doc:`../endpoints/salesforce-object`
.. |fields-to-read| replace:: :doc:`../data-access/value-accessor-sets/salesforce-object`
.. |filters| replace:: :doc:`../filter-expressions/index`
.. |set-use-delta-settings| replace:: :doc:`../../framework/pipeline-steps/set-use-delta-settings`

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Endpoint From``                 | | The |ep| *endpoint* from which objects are read.                    |   
+-----------------------------------+-----------------------------------------------------------------------+
| ``Salesforce Object Name``        | | Name of the object to read from Salesforce.                         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Fields to Read``                | | The fields from the objects that are read from Salesforce.          |
|                                   | |                                                                     |
|                                   | | Fields are specified by selecting one or more                       |
|                                   | | |fields-to-read| *value accessor set* items.                        |
|                                   | |                                                                     |
|                                   | | The selected fields must be defined on the object. If a             |
|                                   | | field is selected that is not defined on the object, an             | 
|                                   | | exception is thrown when the pipeline step runs.                    |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Page Size``                     | | The maximum number of objects that will be read from Salesforce     |
|                                   | | at a time.                                                          |
|                                   | |                                                                     |
|                                   | | If the number of objects that can be read is larger than the page   |
|                                   | | size, multiple calls to Salesforce are made.                        |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Maximum Count``                 | | The maximum number of objects that will be read from Salesforce.    |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Filter Expression``             | | The *filter expression* that controls which entities are read       | 
|                                   | | from CRM.                                                           | 
|                                   | |                                                                     |
|                                   | | See |filters| for more information.                                 |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Exclude Use Delta Settings``    | | By default, a filter is added to the Salesforce query that ensures  |
|                                   | | only object that have been modified within a specific date range    |
|                                   | | are returned.                                                       |
|                                   | |                                                                     |
|                                   | | Ticking this option disables that filter, meaning that the modified |
|                                   | | date on the objects is not considered.                              |
|                                   | |                                                                     |
|                                   | | The date range is determined by the **DateRangeSettings** plugin    |
|                                   | | on the *pipeline context*. If this plugin is not set, this option   |
|                                   | | does not apply.                                                     |
|                                   | |                                                                     |
|                                   | | The plugin is typically set by the |set-use-delta-settings|         |
|                                   | | pipeline step.                                                      |
+-----------------------------------+-----------------------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``DateRangeSettings``             | | If this plugin is available, the date range specified is used to    |
|                                   | | create a filter so that only entities modified within the range     |
|                                   | | are read.                                                           |
+-----------------------------------+-----------------------------------------------------------------------+
| ``IterableDataSettings``          | | Subsequent pipeline steps use this plugin to access the entities    |
|                                   | | read from CRM.                                                      |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
