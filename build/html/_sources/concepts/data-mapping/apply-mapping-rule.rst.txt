Apply Mapping Rule
===================================================

.. |component-description| replace:: An *apply mapping rule* is a component that determines whether a *value mapping* should be applied in a specific context.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Apply Mapping Rules/Base Templates/Base Apply Mapping Rule``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------
The base *apply mapping rule* should not be used on 
its own. It is a base template for specific types of 
*apply mapping rules*.

.. seealso::
    
    For information on the *apply mapping rules* included 
    with the supported providers, see the section 
    :doc:`/component-reference/apply-mapping-rules/index` 
    in the :doc:`/component-reference/index`.

When to Extend
---------------------------------------------------
Data Exchange Framework comes with a set of standard 
*apply mapping rules*. In addition, each provider 
may include a set of *apply mapping rules* designed 
specifically for the system the provider integrates.

Custom *apply mapping rules* can be implemented 
in cases where special logic is needed in order 
to determine whether a *value mapping* should 
be applied.

.. seealso::

    For information on how to implement a custom 
    *apply mapping rules*, see the section 
    :doc:`/cookbooks/custom-apply-mapping-rule/index` 
    in the :doc:`/cookbooks/index`.
