Update Sitecore Item 
=============================

This *pipeline step* is used to update an item in a Sitecore database. If the item
already exists in CRM, the entity is updated. If the item does not already exist in
the Sitecore database, the item is added.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Update Sitecore Item Pipeline Step**                                |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

.. |endpoint| replace:: :doc:`../endpoints/item-model-repo`

+-------------------------------------------------+---------------------------------------------------------+
| Field                                           | Description                                             |
+=================================================+=========================================================+
| ``Endpoint for Sitecore item model repository`` | | The |endpoint| *endpoint* to used to                  |
|                                                 | | update the item.                                      |
+-------------------------------------------------+---------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``SynchronizationSettings``       | | Provides access to the target object, which is the Sitecore item    | 
|                                   | | that is saved.                                                      |
|                                   | |                                                                     |
|                                   | | If this plugin is not set on the pipeline context prior to this     | 
|                                   | | pipeline step running, the pipeline step will abort. This is not a  |
|                                   | | *critical error*.                                                   |
|                                   | |                                                                     |
|                                   | | If no target object is set, or if the object is not the proper      | 
|                                   | | type, the pipeline step will abort. This is not a *critical error*. |
+-----------------------------------+-----------------------------------------------------------------------+
