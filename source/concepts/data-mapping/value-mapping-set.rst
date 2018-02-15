Value Mapping Set
===================================================

.. |component-description| replace:: A *value mapping set* controls the mapping of data from one object to another.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Mapping/Value Mapping Set``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------
A *value mapping set* does not have any settings of its 
own to configure. To associate a :doc:`Value Mappings <value-mapping>` 
with a *value mapping set*, the *value mapping* is added 
as a child.

When to Extend
---------------------------------------------------
The default *value mapping set* depends on the 
*value mappings* assigned to it in order to 
know what data to map.

Custom *value mapping sets* can be implemented in cases 
where the mapping logic is too complex to be described 
through configuration, or when you want to reuse 
existing mapping logic.

For information on how to implement a custom *value mapping set*, 
see the section :doc:`/cookbooks/data-mapping-using-code/index`.
