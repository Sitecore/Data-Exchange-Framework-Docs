Value Accessor
===================================================

.. |component-description| replace:: A *value accessor* is like a property on a .NET class. It provides the ability to read a value and/or write a value.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Value Accessors/Value Accessor``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------
It is rare for the generic *value accessor* to be used.
In most cases, a specific type of *value accessor* is
used (for example, one that represents a property on an object).
The configuration of any specific *value accessor* depends
on its type.

But all *value accessors* inherit the following fields. 
When these fields are used, the will override the default
behavior of the *value accessor*. 

.. |field-01| replace:: Value Reader
.. |description-01| replace:: The *value reader* that is returned when the *value reader* is requested from the *value accessor*.
.. |field-02| replace:: Value Writer
.. |description-02| replace:: The *value writer* that is returned when the *value writer* is requested from the *value accessor*.

+-------------------+-----------------------------+
| Field             | Description                 |
+===================+=============================+
| |field-01|        | |description-01|            |
+-------------------+-----------------------------+
| |field-02|        | |description-02|            |
+-------------------+-----------------------------+

.. seealso::
    
    For information on the *value accessors* included 
    with the supported providers, see the section 
    :doc:`/component-reference/value-accessors/index` 
    in the :doc:`/component-reference/index`.

When to Extend
---------------------------------------------------
Data Exchange Framework comes with a set of standard 
*value accessors*. In addition, each provider comes with
a set of *value accessors* designed specifically for the
system the provider integrates.

The following are cases where custom *value accessors* 
may be needed:

    * A developer building a custom provider that involves working with a 3rd party API.
    * Simplifying configuration by encapsulating complex logic in a single *value accessor*.
