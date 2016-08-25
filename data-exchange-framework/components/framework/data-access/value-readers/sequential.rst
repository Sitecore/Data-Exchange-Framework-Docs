Sequential
==========================================

This *value reader* is used to read a value from a *source object* by 
invoking a series of value readers, where the source object passed 
to each subsequent value reader is the object that was read by the 
previous value reader.

This value reader allows object models to be traversed without 
requiring custom development.

+-----------------+-----------------------------------------------------------+
| Template name   | **Sequential Value Reader**                               |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-reader`                                  |
+-----------------+-----------------------------------------------------------+
