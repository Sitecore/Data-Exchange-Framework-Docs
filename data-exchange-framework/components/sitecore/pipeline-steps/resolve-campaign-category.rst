Resolve Campaign Category
=============================

This *pipeline step* is used to read information used to determine the  
campaign category that is appropriate for the current tenant.

.. note:: 

    Unlike other pipeline steps that resolve something, this
    pipeline step only collects information. The job of
    determining whether or not a new object is needed is
    handled by the :doc:`save-campaign` pipeline step.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve Campaign Category Pipeline Step**                           |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

+-------------------------------------------------+---------------------------------------------------------+
| Field                                           | Description                                             |
+=================================================+=========================================================+
| ``Make campaign category item bucketable``      | | If selected, the category item is set as bucketable   |
|                                                 | | and the campaign items are added to the bucket.       |
|                                                 | |                                                       |
|                                                 | | If not selected, campaign items are added to the      |
|                                                 | | campaign category as child items.                     |
|                                                 | |                                                       |
|                                                 | | Enable this option when you are synchronizing enough  |
|                                                 | | campaigns that having to scroll down a list in order  |
|                                                 | | to find a specific campaign is too difficult.         |
+-------------------------------------------------+---------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``CampaignCategorySettings``      | | Subsequent pipeline steps use this plugin to access the contacts    |
|                                   | | read from xDB.                                                      |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
