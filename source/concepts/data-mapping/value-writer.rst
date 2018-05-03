Value Writer
===================================================

.. |component-description| replace:: A *value writer* is like a property-setter on a .NET class. It provides the implementation of the logic needed to write a value to an object.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Value Writers/Value Writer``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------
It is rare for the generic *value writer* to be used.
In most cases, a specific type of *value writer* is
used (for example, one that can set a property on an object).
The configuration of any specific *value writer* depends
on its type.

.. seealso::
    
    For information on the *value writers* included 
    with the supported providers, see the section 
    :doc:`/component-reference/value-writers/index` 
    in the :doc:`/component-reference/index`.

When to Extend
---------------------------------------------------
Data Exchange Framework comes with a set of standard 
*value writers*. In addition, each provider comes with
a set of *value writers* designed specifically for the
system the provider integrates.

The following are cases where custom *value writers* 
may be needed:

    * A developer building a custom provider that involves working with a 3rd party API.
    * Simplifying configuration by encapsulating complex logic in a single *value writer*.

