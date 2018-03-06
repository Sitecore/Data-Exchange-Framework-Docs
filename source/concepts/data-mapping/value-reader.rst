Value Reader
===================================================

.. |component-description| replace:: A *value reader* is like a property-getter on a .NET class. It provides the implementation of the logic needed to read a value from an object.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Value Readers/Value Reader``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------
It is rare for the generic *value reader* to be used.
In most cases, a specific type of *value reader* is
used (for example, one that can get a property on an object).
The configuration of any specific *value reader* depends
on its type.

.. seealso::
    
    For information on the *value readers* included 
    with the supported providers, see the section 
    :doc:`/component-reference/value-readers/index` 
    in the :doc:`/component-reference/index`.

When to Extend
---------------------------------------------------
Data Exchange Framework comes with a set of standard 
*value readers*. In addition, each provider comes with
a set of *value readers* designed specifically for the
system the provider integrates.

The following are cases where custom *value readers* 
may be needed:

    * A developer building a custom provider that involves working with a 3rd party API.
    * Simplifying configuration by encapsulating complex logic in a single *value reader*.

.. seealso::

    For information on how to implement a custom 
    *value reader*, see the section 
    :doc:`/cookbooks/custom-components/custom-value-reader/index` 
    in the :doc:`/cookbooks/index`.
