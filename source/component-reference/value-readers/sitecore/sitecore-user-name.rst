Sitecore User Name Value Reader
===================================================
This value reader is used to read the user name of a Sitecore user.

.. |source-type-label| replace:: Expected source object type
.. |source-type| replace:: Not applicable. This value reader does not use the source object.
.. |template-location| replace:: **Data Exchange > Providers > Sitecore > Data Access > Value Readers > Sitecore User Value Reader**

+---------------------------+---------------------------------------------------------------------+
| |source-type-label|       | |source-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

.. note::

    This component is not compatible with the remote SDK. 
    It has dependencies on the Sitecore kernel and runtime.

Template Fields
---------------------------------------------------

.. |user| replace:: The Sitecore user whose user name is returned. If no user is specified, the current user at runtime is used.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Sitecore User             | |user|                                                              |
+---------------------------+---------------------------------------------------------------------+
