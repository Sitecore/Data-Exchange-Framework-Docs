Resolve xDB Contact from Queue
=======================================

This *pipeline step* is used to find an instance of 
``Sitecore.Analytics.Model.Entities.IContactTemplate``
in a *work queue*. The *identifier value* from the 
*identifier object* is used to perform the search. 

Based on the pipeline step configuration, a new ``IContactTemplate`` 
may be created if one does not already exist. In this case, the 
identifier object must be a ``Sitecore.Analytics.Tracking.Contact``. 

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve xDB Contact from Queue Pipeline Step**                      |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-resolve-object-from-queue`  |
+-----------------------------------+-----------------------------------------------------------------------+

.. include:: ../../../../common/no-template-fields-added.txt
