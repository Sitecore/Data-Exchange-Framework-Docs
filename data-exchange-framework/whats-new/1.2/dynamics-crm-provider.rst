Dynamics CRM Provider
=================================================

.. contents:: What's new in version 1.2
   :depth: 2
   :local:

Dynamics CRM Provider for Data Exchange Framework
----------------------------------------------------------

Added support for bulk CRM entity update
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A *queue processor* is available for updating multiple CRM 
entities in a single call. For details see 
:doc:`../../components/dynamics-crm/queues/queue-processors/crm-contacts`. 

Updated branch template for creating new tenants
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The following changes were made to :doc:`../../components/dynamics-crm/tenants/dynamics-crm-tenant`:

    * Bulk CRM entity update feature is used when synchronizing xDB contacts with CRM.
    * Bulk Sitecore campaign update feature is used when synchronizing CRM campaigns with Sitecore.
    * *Mappings applied actions* are used to ensure data is updated only when changes are made.

.. note::
    *Tenants* that were created using a previous version of the
    provider are not updated automatically during the update 
    process. 
    
    If you wish to take advantage of these new features, you must 
    either manually change your tenant's configuration, or create 
    a new tenant. 

CRM Connect
----------------------------------------------------------

Moved from Dynamics CRM Provider for CRM Connect
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Condition for segment builder that test marketing list membership.
    * Condition for personalization that test marketing list membership.
    * Sitecore definition item that represents an external marketing list.
       
API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Added async support on ``IRepository``.

Dynamics CRM Provider for CRM Connect
----------------------------------------------------------

New features
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Configuration file for Azure search provider.

Moved to CRM Connect
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Condition for segment builder that test marketing list membership.
    * Condition for personalization that test marketing list membership.
    * Sitecore definition item that represents an external marketing list.

API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Renamed the interface and implementation for the custom 
      facet used to store basic data from Dynamics CRM in xDB.
    * Implemented async support on ``XrmClientEntityRepository``.
    * Added ``SupportedIdsAttribute`` to simplify the process of implementing converters.


