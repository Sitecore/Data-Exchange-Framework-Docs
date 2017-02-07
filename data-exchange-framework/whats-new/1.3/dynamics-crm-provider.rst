Dynamics CRM Provider
=================================================

.. contents:: What's new in version 1.3
   :depth: 2
   :local:

Dynamics CRM Provider for Data Exchange Framework
----------------------------------------------------------

API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Renamed namespace ``Sitecore.DataExchange.Providers.DynamicsCrm.ApplyMappingStatusActions`` to ``Sitecore.DataExchange.Providers.DynamicsCrm.MappingsAppliedActions``.
    * Renamed namespace ``Sitecore.DataExchange.Providers.DynamicsCrm.Converters.ApplyMappingStatusActions`` to ``Sitecore.DataExchange.Providers.DynamicsCrm.Converters.MappingsAppliedActions``.

Bugs fixes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * Filter expression with operator "On or before selected" date does not work (131540)
    * Default entity name is set on template used to update any entity (137924)
    * Certain *pipeline steps* are not included in the insert options for the *pipeline* template (137924)
    * *Pipeline step* template has incorrect name (138275)
    * Unable to write option set values to Dynamics entities (139650)

CRM Connect
----------------------------------------------------------

None.

Dynamics CRM Provider for CRM Connect
----------------------------------------------------------

None.