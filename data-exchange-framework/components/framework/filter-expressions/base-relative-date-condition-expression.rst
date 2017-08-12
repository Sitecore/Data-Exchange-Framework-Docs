Base Relative Date Condition Expression
==========================================

This template is the base template for *filter expressions* that 
compares a value to a date that is relative to a known date.

.. include:: ../../../../common/base-template-always-inherit-notice.txt

The following are examples of relative date conditions:

    * Within the last week
    * Within the next 30 days

A relative date condition expression is implemented as a dynamically 
generated date range condition. To use the examples above:

+---------------------------+------------------------------+------------------------------+
| Description               | Start date                   | End date                     |
+===========================+==============================+==============================+
| Within the last week      | Today - 7 days               | Today                        |
+---------------------------+------------------------------+------------------------------+
| Within the next 30 days   | Today                        | Today + 30 days              |
+---------------------------+------------------------------+------------------------------+

+-----------------+-----------------------------------------------------------+
| Template name   | **Base Relative Date Condition Expression**               |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-condition-expression`                    |
+-----------------+-----------------------------------------------------------+

+--------------------------+--------------------------------------------------------------------------------+
| Field                    | Description                                                                    |
+==========================+================================================================================+
| ``Operator``             | | This value is used to determine the start and end dates for the              |
|                          | | condition expression.                                                        |
+--------------------------+--------------------------------------------------------------------------------+
| ``Offset``               | | The integer value that is used to determine the start and end dates          | 
|                          | | for the condition expression.                                                |
|                          | |                                                                              |
|                          | | When this is a negative number, a date in the past is used. When this        |
|                          | | is a positive number, a date in the future is used.                          |
+--------------------------+--------------------------------------------------------------------------------+
| ``Unit of Time``         | | This value is used to determine the start and end dates for the              | 
|                          | | condition expression.                                                        |
+--------------------------+--------------------------------------------------------------------------------+

