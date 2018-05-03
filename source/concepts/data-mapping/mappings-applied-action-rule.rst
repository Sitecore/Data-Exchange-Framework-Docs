Mappings Applied Action Rule
===================================================

.. |component-description| replace:: A *mappings applied action rule* is a component that determine whether a specific :doc:`mappings-applied-action` is run.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Mappings Applied Action Rules/Base Templates/Base Mappings Applied Action Rule``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------
The base *mappings applied action rule* should not be used on 
its own. It is a base template for specific types of 
*mappings applied action rules*.

.. seealso::
    
    For information on the *mappings applied action rules* included 
    with the supported providers, see the section 
    :doc:`/component-reference/mappings-applied-action-rules/index` 
    in the :doc:`/component-reference/index`.

When to Extend
---------------------------------------------------
Data Exchange Framework comes with a set of standard 
*mappings applied action rules*. In addition, each provider 
may include a set of *mappings applied action rules* designed 
specifically for the system the provider integrates.

Custom *mappings applied action rules* can be implemented 
in cases where special logic is needed in order 
to determine whether a *mappings applied action* 
should run.
