Default Value Apply Mapping Rule
===================================================
This rule is used to ensure a value is not the default value.

The rule uses the value's type in order to determine what
the default value is. This enables value types and object
types to be supported.

This rule is usually used to prevent actual values with 
default values. For example, imagine you are trying to 
update the phone number on an existing contact. The 
phone number is stored as a string. The contact already
has a phone number specified, but the source object
does not have a phone number set on it. This rule can 
be used to ensure the existing phone number is not 
overwritten with a null string.

.. |value-type-label| replace:: Expected type of the value being written to the target object
.. |value-type| replace:: ``System.Object``
.. |template-location| replace:: **Data Exchange > Apply Mapping Rules > Default Value Mapping Rule**

+---------------------------+---------------------------------------------------------------------+
| |value-type-label|        | |value-type|                                                        |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------
This template has no fields on it.