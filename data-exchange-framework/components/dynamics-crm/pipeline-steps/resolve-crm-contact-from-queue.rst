Resolve CRM Contact From Queue
===============================

This *pipeline step* is used to find an instance of 
``Microsoft.Xrm.Sdk.Entity`` in a Dynamics CRM instance. 
The *identifier value* from the *identifier object* is 
used to perform the search. 

Based on the pipeline step configuration, a new ``Entity`` 
may be created if one does not already exist. 

This *pipeline step* is used to find an entity in Dynamics CRM by matching 
an attribute value.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve CRM Contact from Queue Pipeline Step**                      |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-resolve-object-from-queue`  |
+-----------------------------------+-----------------------------------------------------------------------+

.. include:: ../../../../common/no-template-fields-added.txt
