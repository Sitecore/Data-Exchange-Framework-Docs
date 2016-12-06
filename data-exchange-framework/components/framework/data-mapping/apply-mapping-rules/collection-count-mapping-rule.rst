Collection Count
==========================================

This *apply mapping rule* is used to ensure that a collection has a certain number of elements.

+-----------------+-----------------------------------------------------------+
| Template name   | **Collection Count Mapping Rule**                         |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-apply-mapping-rule`                            |
+-----------------+-----------------------------------------------------------+

+--------------------------------------+--------------------------------------------------------------------+
| Field                                | Description                                                        |
+======================================+====================================================================+
| ``Minimum Count``                    | | The collection must contain at least this many elements.         |
|                                      | |                                                                  |
|                                      | | ``0`` means that any number of elements is allowed, provided     |
|                                      | | the number does not exceed the value of the ``Maximum Count``    |
|                                      | | field.                                                           |
+--------------------------------------+--------------------------------------------------------------------+
| ``Maximum Count``                    | | The collection may not contain any more than this many elements. |
|                                      | |                                                                  |
|                                      | | ``-1`` means an unlimited number elements is allowed.            |  
+--------------------------------------+--------------------------------------------------------------------+
