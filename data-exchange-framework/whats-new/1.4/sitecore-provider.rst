Sitecore Provider
=================================================

.. contents:: What's new in version 1.4
   :depth: 2
   :local:

New features
-----------------------------

Enhanced support for reading from and writing to Sitecore items
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A *value transformer* is a *value reader* that is used to transform a value
after it has been read or before it has been written. They are used in cases 
where the value read or that will be written needs to be converted into 
another format before it can be used in a synchronization process.

This feature is used for things such as handling guid values in Sitecore.
Usually when a field value is a guid it means the field value is a reference
to a Sitecore item. But when data from an external system is stored in 
Sitecore item fields, it is possible that the guid represents an identifier 
in the external system instead.

During a synchronization process, it may be important for the value to be 
a guid. A *value transformer* can be used to ensure the string value 
stored in Sitecore is converted into a guid when the value is read
from the Sitecore item within a synchronization process.

Additionally, a *value transform* can be used to ensure the guid is 
converted into a string before the value is written to a Sitecore item.

For more details, see 
:doc:`../../components/sitecore/data-access/value-accessors/item-field-value`.

API changes
-----------------------------

    * :download:`Sitecore.DataExchange.Providers.Sc.dll <_static/Sitecore.DataExchange.Providers.Sc.dll 1.3 to 1.4.html>`
    * :download:`Sitecore.DataExchange.Providers.Sc.Local.dll <_static/Sitecore.DataExchange.Providers.Sc.Local.dll 1.3 to 1.4.html>`

Bugs fixes
-----------------------------

    * Wrong base template for ``Sitecore Value Accessor Sets Root``. (156424)
