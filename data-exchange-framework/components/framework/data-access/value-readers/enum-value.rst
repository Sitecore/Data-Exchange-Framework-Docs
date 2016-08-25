Enum Value
==========================================

This *value reader* is used to read a value as a member of a .NET enum.

This value reader supports a number of formats:

    * An ``int`` value will be converted into the enum member with a matching name. If the value does not correspond with an enum member, null is returned.
    * A ``string`` value will be converted into the enum member with a matching name. If the name does not correspond with an enum member, null is reteurned. 

+-----------------+-----------------------------------------------------------+
| Template name   | **Enum Value Reader**                                     |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-reader`                                  |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Enum type``                                 | The type of the enum to read.                             |
+-----------------------------------------------+-----------------------------------------------------------+
