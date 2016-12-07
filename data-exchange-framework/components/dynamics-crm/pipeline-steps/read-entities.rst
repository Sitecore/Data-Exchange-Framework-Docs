Read CRM Entities
=============================

This *pipeline step* is used to read entities from Dynamics CRM.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Read CRM Entities Pipeline Step**                                   |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

.. |ep| replace:: :doc:`../endpoints/crm-entities`
.. |attributes-to-read| replace:: :doc:`../data-access/value-accessor-sets/entity-attributes`
.. |filters| replace:: :doc:`../crm-filter-expressions/index`
.. |set-use-delta-settings| replace:: :doc:`set-use-delta-settings`

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Endpoint From``                 | | The |ep| *endpoint* from which entities are read.                   |   
+-----------------------------------+-----------------------------------------------------------------------+
| ``Entity Name``                   | | Name of the entity to read from CRM.                                |
|                                   | |                                                                     |
|                                   | | The *entity repository set* assigned to the endpoint must be        | 
|                                   | | configured to support the specified entity.                         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Attributes to Read``            | | The attributes from the entities that are read from CRM.            |
|                                   | |                                                                     |
|                                   | | Attributes are specified by selecting one or more                   |
|                                   | | |attributes-to-read| *value accessor set* items.                    |
|                                   | |                                                                     |
|                                   | | The selected attributes must be defined on the entity. If an        |
|                                   | | attribute is selected that is not defined on the entity, an         | 
|                                   | | exception is thrown when the pipeline step runs.                    |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Page Size``                     | | The maximum number of entities that will be read from CRM at        |
|                                   | | a time.                                                             |
|                                   | |                                                                     |
|                                   | | If the number of entities that can be read is larger than the page  |
|                                   | | size, multiple calls to CRM are made.                               |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Maximum Count``                 | | The maximum number of entities that will be read from CRM.          |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Exclude Active Filter``         | | By default, a filter is added to the CRM query that ensures only    |
|                                   | | active entities are returned.                                       |
|                                   | |                                                                     |
|                                   | | Ticking this option disables that filter, meaning that inactive     |
|                                   | | entities may be read.                                               |
|                                   | |                                                                     |
|                                   | | You must use this setting when ``Active`` is not a valid state code |
|                                   | | for the specified entity.                                           |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Filter Expression``             | | The *filter expression* that controls which entities are read       | 
|                                   | | from CRM.                                                           | 
|                                   | |                                                                     |
|                                   | | See |filters| for more information.                                 |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Exclude Use Delta Settings``    | | By default, a filter is added to the CRM query that ensures only    |
|                                   | | entities what have been modified within a specific date range are   |
|                                   | | returned.                                                           |
|                                   | |                                                                     |
|                                   | | Ticking this option disables that filter, meaning that the modified |
|                                   | | date on the entities is not considered.                             |
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
