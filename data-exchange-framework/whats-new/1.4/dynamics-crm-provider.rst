Dynamics CRM Provider
=================================================

.. contents:: What's new in version 1.4
   :depth: 2
   :local:

Dynamics CRM Provider for Data Exchange Framework
----------------------------------------------------------

New features
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * *Mappings applied action rule* is used to ensure *work queue* entry status is set properly.
    * Work queue functionality is used in the process that synchronizes CRM marketing lists with Sitecore items.

API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * :download:`Sitecore.DataExchange.Providers.DynamicsCrm.dll <_static/Sitecore.DataExchange.Providers.DynamicsCrm.dll 1.3 to 1.4.html>`
    * :download:`Sitecore.DataExchange.Providers.DynamicsCrm.Local.dll <_static/Sitecore.DataExchange.Providers.DynamicsCrm.Local.dll 1.3 to 1.4.html>`

Bugs fixes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Last synced property on the CRM Lists to xDB Sync Pipeline Batch is not updated (153786)

----------------------------------------------------------

CRM Connect
----------------------------------------------------------

New features
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Repository interface supports async operations.

API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * :download:`Sitecore.Connect.Crm.dll <_static/Sitecore.Connect.Crm.dll 1.3 to 1.4.html>`

----------------------------------------------------------

Dynamics CRM Provider for CRM Connect
----------------------------------------------------------

New features
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Error handling can be configured to continue or abort on multiple-object operations ``InsertObjects``, ``UpdateObjects``, and ``UpsertObjects`` using the plugin ``MultipleOperationsSettings``.

Bugs fixes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Only the first 5000 marketing lists are synchronized (157184)

API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * :download:`Sitecore.Connect.Crm.DynamicsCrm.dll <_static/Sitecore.Connect.Crm.DynamicsCrm.dll 1.3 to 1.4.html>`
