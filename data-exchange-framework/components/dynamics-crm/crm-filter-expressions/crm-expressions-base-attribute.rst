Base Entity Attribute Value Condition Expression
======================================================

This template is the base template for all CRM expression filters 
that involve an entity attribute.

.. tip:: 
    
    Items based on this template are converted into instances of the 
    type ``Microsoft.Xrm.Sdk.Query.ConditionExpression``. For more 
    information see `<https://msdn.microsoft.com/en-us/library/gg334419.aspx>`_.

.. include:: ../../../../common/base-template-always-inherit-notice.txt

+-----------------+-----------------------------------------------------------+
| Template name   | **Base Entity Attribute Value Condition Expression**      |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+--------------------------+--------------------------------------------------------------------------------+
| Field                    | Description                                                                    |
+==========================+================================================================================+
| ``Value Accessor``       | | The value accessor that is used to read the value of an attribute            |
|                          | | from an entity.                                                              |
|                          | |                                                                              |
|                          | | It is important that the value accessor selected has a field that            |
|                          | | identifies the attribute name. The attribute name is used to build           |
|                          | | the filter for the API call to Dynamics CRM.                                 |
+--------------------------+--------------------------------------------------------------------------------+

