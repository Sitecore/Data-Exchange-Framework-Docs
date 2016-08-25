Resolve Campaign
=============================

This *pipeline step* is used to find an instance of 
``Sitecore.Marketing.Definitions.Campaigns.Data.CampaignActivityDefinitionRecord``  
in a *campaign definition repository*. The *identifier value* from the 
*identifier object* is used to perform the search. 

Based on the pipeline step configuration, a new ``CampaignActivityDefinitionRecord`` 
may be created if one does not already exist. In this case, 
the identifier value is used as the campaign identifier. 
Therefore, the identifier value must be a valid constructor 
argument for ``Sitecore.Data.ID``.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve Marketing Campaign Pipeline Step**                          |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-resolve-object-from-queue`  |
+-----------------------------------+-----------------------------------------------------------------------+

.. include:: ../../../../common/no-template-fields-added.txt

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``CampaignRepositorySettings``    | | Subsequent pipeline steps use this plugin to access the repository  |
|                                   | | used to resolve the campaign.                                       |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
