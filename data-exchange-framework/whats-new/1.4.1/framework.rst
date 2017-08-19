Data Exchange Framework
=================================================

.. important:: 

    There are no breaking changes included in this version.
    The new version number is required in order to match the 
    version numbers for some of the Data Exchange Framework
    providers that do include breaking API changes.

.. contents:: What's new in version 1.4.1
   :depth: 2
   :local:

New features
-----------------------------

Dependent Tree Rule Editor Macro
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Added the macro for the rule editor that allows you to define 
dependencies between properties on a condition or action.
(This functionality was previously included in Sitecore.Connect.Crm.Local.dll.)

API changes 
-----------------------------
    * :download:`Sitecore.DataExchange.Local.dll <_static/Sitecore.DataExchange.Local.dll 1.4.0 to 1.4.1.html>`
    * :download:`Sitecore.Connect.Crm.Local.dll <_static/Sitecore.Connect.Crm.Local.dll 1.4.0 to 1.4.1.html>`

Bugs fixes
-----------------------------

    * ``ObjectsAreNotEqualRule`` is missing a null check. (164581)
    * Filter expression templates are missing. (178440)
