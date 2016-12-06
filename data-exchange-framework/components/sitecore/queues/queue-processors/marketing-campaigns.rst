Marketing Campaigns
==========================================

This *queue processor* is reads marketing campaigns from the queue and writes 
those campaigns to Sitecore.

+-----------------+------------------------------------------------------------------------+
| Template name   | **Queue Processor for Marketing Campaigns**                            |
+-----------------+------------------------------------------------------------------------+
| Base template   | :doc:`../../../framework/queues/queue-processors/base-queue-processor` |
+-----------------+------------------------------------------------------------------------+

This queue processor handles the following types of queue entries:

    * ``Sitecore.Marketing.Definitions.Campaigns.Data.CampaignActivityDefinitionRecord``