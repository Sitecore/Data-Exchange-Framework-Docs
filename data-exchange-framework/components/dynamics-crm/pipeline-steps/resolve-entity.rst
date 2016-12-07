Resolve CRM Entity
=============================

This *pipeline step* is used to find an instance of 
``Microsoft.Xrm.Sdk.Entity`` in a Dynamics CRM instance. 
The *identifier value* from the *identifier object* is 
used to perform the search. 

Based on the pipeline step configuration, a new ``Entity`` 
may be created if one does not already exist. 

This *pipeline step* is used to find an entity in Dynamics CRM by matching 
an attribute value.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve CRM Entity Pipeline Step**                                  |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-resolve-object`             |
+-----------------------------------+-----------------------------------------------------------------------+

.. |endpoint| replace:: :doc:`../endpoints/crm-entities`
.. |attributes-to-read| replace:: :doc:`../data-access/value-accessor-sets/entity-attributes`

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Endpoint From``                 | | The |endpoint| *endpoint* to read an entity from.                   |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Entity Name``                   | | Name of the entity to read from CRM.                                |
|                                   | |                                                                     |
|                                   | | The *entity repository set* assigned to the endpoint must be        |
|                                   | | configured to support the specified entity.                         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Entity Lookup Attribute Name``  | | A query is built that looks for an entity with an attribute whose   |
|                                   | | value matches the identifier value. This field specifies which      |
|                                   | | attribute on the entity is used in the query.                       |
|                                   | |                                                                     |
|                                   | | The selected attribute must be defined on the entity. If an         |
|                                   | | attribute is selected that is not defined on the entity, an         |
|                                   | | exception is thrown when the pipeline step runs.                    |
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
| ``Exclude Active Filter``         | | By default, a filter is added to the CRM query that ensures only    |
|                                   | | active entities are returned.                                       |
|                                   | |                                                                     |
|                                   | | Ticking this option disables that filter, meaning that inactive     |
|                                   | | entities may be read.                                               |
|                                   | |                                                                     |
|                                   | | You must use this setting when ``Active`` is not a valid state      |
|                                   | | code for the specified entity.                                      |
+-----------------------------------+-----------------------------------------------------------------------+
