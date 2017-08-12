Resolve Salesforce Object
=============================

This *pipeline step* is used to find an instance of 
``Salesforce.Common.Models.Xml.SObject`` in a Salesforce 
instance. The *identifier value* from the *identifier object* 
is used to perform the search. 

Based on the pipeline step configuration, a new ``SObject`` 
may be created if one does not already exist. 

This *pipeline step* is used to find an object in Salesforce 
by matching a field value.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve CRM Entity Pipeline Step**                                  |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-resolve-object`             |
+-----------------------------------+-----------------------------------------------------------------------+

.. |endpoint| replace:: :doc:`../endpoints/salesforce-object`
.. |fields-to-read| replace:: :doc:`../data-access/value-accessor-sets/salesforce-object`
.. |salesforce-object| replace:: :doc:`../data-access/value-accessor-sets/salesforce-object`

+-----------------------------------------+-----------------------------------------------------------------------+
| Field                                   | Description                                                           |
+=========================================+=======================================================================+
| ``Endpoint From``                       | | The |endpoint| *endpoint* to read an object from.                   |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Salesforce Object Name``              | | Name of the object to read from Salesforce.                         |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Salesforce Object Lookup Field Name`` | | A query is built that looks for an object with a field whose        |
|                                         | | value matches the identifier value. This field specifies which      |
|                                         | | field on the object is used in the query.                           |
|                                         | |                                                                     |
|                                         | | The selected field must be defined on the object. If a              |
|                                         | | field is selected that is not defined on the object, an             |
|                                         | | exception is thrown when the pipeline step runs.                    |
+-----------------------------------------+-----------------------------------------------------------------------+
| ``Fields to Read``                      | | The fields from the objects that are read from Salesforce.          |
|                                         | |                                                                     |
|                                         | | Fields are specified by selecting one or more                       |
|                                         | | |fields-to-read| *value accessor set* items.                        |
|                                         | |                                                                     |
|                                         | | The selected fields must be defined on the object. If a             |
|                                         | | field is selected that is not defined on the object, an             |
|                                         | | exception is thrown when the pipeline step runs.                    |
+-----------------------------------------+-----------------------------------------------------------------------+
