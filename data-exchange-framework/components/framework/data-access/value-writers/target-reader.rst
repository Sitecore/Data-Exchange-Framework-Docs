Target Reader
==========================================

This *value writer* is used to read one .NET object and write the value to a different object.

Consider a case where you are populating an object with a property that represents a person.
You want to set the person's address. In order to set the address, first you must read the address
object from the person. Then you can write the address to that object.

This value writer allows you to specify the value reader used to read the address object from the person.
It also allows you to specify the value writer used to write the address to the address object. 

To do this you must define a new *value accessor*. The *value reader* on the value accessor specifies
the value reader to use. The value writer on the value accessor specifies the value writer to use.

+-----------------+-----------------------------------------------------------+
| Template name   | **Target Reader Value Writer**                            |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-writer`                                  |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Value Accessor``                            | | The *value accessor* that provides the value reader     |
|                                               | | that reads the object that is written to, and the       |
|                                               | | value writer that is used to write the value to that    |
|                                               | | object.                                                 |
+-----------------------------------------------+-----------------------------------------------------------+
