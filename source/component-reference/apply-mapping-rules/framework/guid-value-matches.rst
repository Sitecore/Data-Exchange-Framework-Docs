Guid Value Matches Apply Mapping Rule
===================================================
This rule is used to ensure a value is a guid and 
that is either matches or does not match specified
guids.

.. |value-type-label| replace:: Expected type of the value being written to the target object
.. |value-type| replace:: ``System.Guid``
.. |template-location| replace:: **Data Exchange > Apply Mapping Rules > Guid Value Matches Mapping Rule**

+---------------------------+---------------------------------------------------------------------+
| |value-type-label|        | |value-type|                                                        |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |req-source| replace:: The value read from the source object must match one of the specified guids.
.. |no-source| replace:: The value read from the source object must not match any of the specified guids.
.. |source-transformer| replace:: The value read from the source object is transformed using this component before it is compared to the required and disallowed source values.
.. |req-target| replace:: The value read from the target object must match one of the specified guids.
.. |no-target| replace:: The value read from the target object must not match any of the specified guids.
.. |target-transformer| replace:: The value read from the target object is transformed using this component before it is compared to the required and disallowed target values.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Required Source Values    | |req-source|                                                        |
+---------------------------+---------------------------------------------------------------------+
| Disallowed Source Values  | |no-source|                                                         |
+---------------------------+---------------------------------------------------------------------+
| Source Value Transformer  | |source-transformer|                                                |
+---------------------------+---------------------------------------------------------------------+
| Required Target Values    | |req-target|                                                        |
+---------------------------+---------------------------------------------------------------------+
| Disallowed Target Values  | |no-target|                                                         |
+---------------------------+---------------------------------------------------------------------+
| Target Value Transformer  | |target-transformer|                                                |
+---------------------------+---------------------------------------------------------------------+
