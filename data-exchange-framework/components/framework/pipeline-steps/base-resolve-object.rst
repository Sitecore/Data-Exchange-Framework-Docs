Base Resolve Object
==========================================

This template is the base template for any *pipeline step* that 
searches for an existing object that matches an identifier value.

.. include:: ../../../../common/base-template-always-inherit-notice.txt

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Base Resolve Object Pipeline Step**                                 |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`base-pipeline-step`                                             |
+-----------------------------------+-----------------------------------------------------------------------+

+-------------------------------------------------------------+---------------------------------------------+
| Field                                                       | Description                                 |
+=============================================================+=============================================+
| ``Identifier Value Accessor``                               | | *Value accessor* used to read the         |
|                                                             | | identifier from the identifier object.    |  
+-------------------------------------------------------------+---------------------------------------------+
| ``Identifier Object Location``                              | | Where the identifier object is found.     |
+-------------------------------------------------------------+---------------------------------------------+
| ``Value Reader to Convert Identifier Value for Comparison`` | | *Value reader* used to convert the        |
|                                                             | | identifier value into a format so it can  |
|                                                             | | be compared. What the identifier value    |
|                                                             | | is compared to depends on the type that   |
|                                                             | | inherits from this template.              |
+-------------------------------------------------------------+---------------------------------------------+
| ``Finish Pipeline If Object Not Resolved``                  | | By default, if the identifier object is   |
|                                                             | | not resolved, the *pipeline* will continue|
|                                                             | | running. This setting can prevent         |
|                                                             | | subsequent pipeline steps from running.   |
+-------------------------------------------------------------+---------------------------------------------+
| ``Do Not Create If Object Not Resolved``                    | | By default, if the identifier object is   |
|                                                             | | not resolved, the pipeline step will try  |
|                                                             | | to create a new object. This setting can  |
|                                                             | | prevent a new object from being created.  |
+-------------------------------------------------------------+---------------------------------------------+
| ``Resolved Object Location``                                | | If the object is resolved, this           |
|                                                             | | setting specified where the object is     |
|                                                             | | stored so it is available to subsequent   |
|                                                             | | pipeline steps.                           |
+-------------------------------------------------------------+---------------------------------------------+

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
+-----------------------------------+-----------------------------------------------------------------------+