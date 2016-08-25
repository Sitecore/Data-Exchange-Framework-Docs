Resolve xDB Contact from Repository
=======================================

This *pipeline step* is used to find an instance of 
``Sitecore.Analytics.Tracking.Contact`` in a 
*contact repository*. The *identifier value* from the 
*identifier object* is used to perform the search. 

Based on the pipeline step configuration, a new ``Contact`` 
may be created if one does not already exist. In this case, 
the identifier value is used as the contact identifier.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve xDB Contact from Repository Pipeline Step**                 |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`base-resolve-object`                                            |
+-----------------------------------+-----------------------------------------------------------------------+

.. include:: ../../../../common/no-template-fields-added.txt
