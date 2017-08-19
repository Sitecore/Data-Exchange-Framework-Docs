Dependent Tree Macro
=======================================

This *macro* allows you to define dependencies between parameters 
in a condition or action.

For example, this macro is used to ensure that components under 
a *tenant* can only access other components in the same tenant.
Such as when you select an *endpoint* in a *pipeline step*. The 
endpoints that are available depend on the tenant being configured.

.. note:: 

    This macro is defined in the following location:

    **sitecore > system > Settings > Rules > Definitions > Macros > Data Exchange Framework > DependentTree**

+---------------------------+---------------------------------------------------------------------+
| Attribute                 | Description                                                         |
+===========================+=====================================================================+
| ``dependency``            | | Name of another property on the condition or action.              |
+---------------------------+---------------------------------------------------------------------+
| ``mode``                  | | Determines how the root item for the tree is determined. The      |
|                           | | following values are valid:                                       |
|                           | |                                                                   |
|                           | | ``descendant`` - Find the first descendant of the item selected   |
|                           | | in the **dependency** property that is based on the template      |
|                           | | specified by the **templateid** attribute. Then the first child   |
|                           | | whose name matches the value of the **rootitemname** attribute.   |
|                           | | Use this item as the root for the tree.                           |
+---------------------------+---------------------------------------------------------------------+
| ``templateid``            | | The purpose of this value depends on the **mode** attribute.      |
+---------------------------+---------------------------------------------------------------------+
| ``rootitemname``          | | The purpose of this value depends on the **mode** attribute.      |
+---------------------------+---------------------------------------------------------------------+
| ``selection``             | | If set to a template id, only items based on the specified        |
|                           | | template id can be selected.                                      |
|                           | |                                                                   |
|                           | | If no value is set, any item displayed in the tree can be         | 
|                           | | selected.                                                         |
+---------------------------+---------------------------------------------------------------------+
| ``setRootAsSearchRoot``   | | This ensure the search dialog uses the root of the tree as the    |
|                           | | root for searches. This attribute must be set to ``true``.        |
+---------------------------+---------------------------------------------------------------------+

.. caution:: 

    Attribute names are case-sensitive.

.. tip:: 

    This macro can be used beyond Data Exchange Framework. It can be
    used with any Sitecore condition or action. 


