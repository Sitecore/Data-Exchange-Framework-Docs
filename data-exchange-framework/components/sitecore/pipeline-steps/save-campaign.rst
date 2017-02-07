Save Marketing Campaign 
=============================

This *pipeline step* is used to save a marketing campaign in 
Sitecore directly (as opposed to using a *work queue*).

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Save Marketing Campaign Pipeline Step**                             |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

.. include:: ../../../../common/no-template-fields-added.txt

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``SynchronizationSettings``       | | Provides access to the target object, which is the *campaign*       | 
|                                   | | *activity record* that is saved.                                    |
|                                   | |                                                                     |
|                                   | | If this plugin is not set on the pipeline context prior to this     | 
|                                   | | pipeline step running, the pipeline step will abort. This is not a  |
|                                   | | *critical error*.                                                   |
|                                   | |                                                                     |
|                                   | | If no target object is set, or if the object is not the proper      | 
|                                   | | type, the pipeline step will abort. This is not a *critical error*. |
+-----------------------------------+-----------------------------------------------------------------------+
| ``CampaignRepositorySettings``    | | Provides access to the *campaign repository* that is used to save   |
|                                   | | the campaign.                                                       |
|                                   | |                                                                     |
|                                   | | If this plugin is not set on the pipeline context prior to this     | 
|                                   | | pipeline step running, the pipeline step will abort. This is not a  |
|                                   | | *critical error*.                                                   |
|                                   | |                                                                     |
|                                   | | If no campaign repository is set, or if the object is not the       | 
|                                   | | proper type, the pipeline step will abort. This is not a *critical* |
|                                   | | *error*.                                                            |
+-----------------------------------+-----------------------------------------------------------------------+
| ``CampaignCategorySettings``      | | Provides access to the settings that determine the category the     |
|                                   | | campaign is saved to.                                               |
|                                   | |                                                                     |
|                                   | | If this plugin is not set on the pipeline context prior to this     | 
|                                   | | pipeline step running, the pipeline step will abort. This is not a  |
|                                   | | *critical error*.                                                   |
+-----------------------------------+-----------------------------------------------------------------------+
