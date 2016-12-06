Default Value
==========================================

This *apply mapping rule* is used to ensure that default values can be ignored 
during the mapping process.

The default value depends on the value being read from the source object. 

For example, if an ``int`` is read, this apply mapping rule will prevent the 
value ``0`` from being written to the target object. If a ``string`` is read,
this apply mapping rule will prevent ``null`` from being written to the target
object. 

+-----------------+-----------------------------------------------------------+
| Template name   | **Default Value Mapping Rule**                            |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-apply-mapping-rule`                            |
+-----------------+-----------------------------------------------------------+

