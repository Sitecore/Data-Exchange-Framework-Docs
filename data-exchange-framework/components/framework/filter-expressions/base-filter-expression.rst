Base Filter Expression
==========================================

This is the "top-level" item for the definition of a filter expression. 
One or more expressions must be added as children.

Adding a filter expression as a child of another filter expression gives 
you the ability to build more complex expressions. For example, you can 
build an expression that includes contacts whose email address contains 
"example.com" or "example.org" and whose region is "Europe".

.. include:: ../../../../common/base-template-always-inherit-notice.txt

+-----------------+-----------------------------------------------------------+
| Template name   | **Base Filter Expression**                                |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+--------------------------+--------------------------------------------------------------------------------+
| Field                    | Description                                                                    |
+==========================+================================================================================+
| ``Logical Operator``     | | This value determines the relationship between the child expressions:        |
|                          | |                                                                              |
|                          | |  * **And** means that all of the child expressions must be true              |
|                          | |  * **Or** means that at least one of the child expressions must be true      |
+--------------------------+--------------------------------------------------------------------------------+

