Save xDB Contact 
=============================

This *pipeline step* is used to save an xDB contact directly (as opposed 
to using a *work queue*). 

The *target object* on the *pipeline context* must be a 
``Sitecore.Analytics.Tracking.Contact`` object.

.. note:: 

    The default configuration for Dynamics CRM Connect does not use
    this pipeline step. It is provided so that custom pipelines
    can be configured.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Save xDB Contact Pipeline Step**                                    |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

.. |endpoint| replace:: :doc:`../endpoints/local-xdb-contacts`

+-------------------------------------------------+---------------------------------------------------------+
| Field                                           | Description                                             |
+=================================================+=========================================================+
| ``Endpoint for xDB contact repository``         | | The |endpoint| *endpoint* to save the contact to.     |
+-------------------------------------------------+---------------------------------------------------------+
| ``Lease owner name``                            | | When an xDB contact is saved, a lease is used to      |
|                                                 | | lock the contact. This value is the name that appears |
|                                                 | | in xDB to indicate the contact is being updated.      |
+-------------------------------------------------+---------------------------------------------------------+

