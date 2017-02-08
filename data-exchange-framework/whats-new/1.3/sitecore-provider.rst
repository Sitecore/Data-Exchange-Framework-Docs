Sitecore Provider
=================================================

.. contents:: What's new in version 1.3
   :depth: 2
   :local:

New features
-----------------------------

Added support for multiple languages when working with Sitecore items
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

It is possible to set a value on a specific language version of a 
Sitecore item. Prior to this release, all field values were written 
to the default language version. For more details, see 
:doc:`../../cookbooks/synchronization/writing-multilanguage-content-to-sitecore-items/index`

It is also possible to read a value from a specific language version
of a Sitecore item. Prior to this release, all field values were read
from the default language version. For more details, see 
:doc:`../../cookbooks/synchronization/reading-multilanguage-content-from-sitecore-items/index`

API changes
-----------------------------

    * Renamed namespace from ``Sitecore.DataExchange.Providers.Sc.Local.ApplyMappingActions`` to ``Sitecore.DataExchange.Providers.Sc.Local.MappingsAppliedActions``.

