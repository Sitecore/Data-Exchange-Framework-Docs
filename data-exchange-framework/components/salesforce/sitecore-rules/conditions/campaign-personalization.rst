Campaign Personalization
====================================================

This *condition* allows you to define a personalization rule  
that includes or excludes contacts based on membership in
Salesforce campaigns. 

.. note:: 

    This condition is defined in the following location:

    **sitecore > system > Settings > Rules > Definitions > Elements > Salesforce Visitor > Salesforce Campaign**

+---------------------------+---------------------------------------------------------------------+
| Property                  | Description                                                         |
+===========================+=====================================================================+
| ``campaign``              | | The Sitecore item that represents the Salesforce campaign.        |
|                           | |                                                                   |
|                           | | This value is dependent on **tenant**.                            |
+---------------------------+---------------------------------------------------------------------+
| ``tenant``                | | The tenant under which the Salesforce campaign was synchronzied.  |
+---------------------------+---------------------------------------------------------------------+
