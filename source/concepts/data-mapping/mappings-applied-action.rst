Mappings Applied Action
===================================================

.. |component-description| replace:: A *mappings applied action* is a component that represents logic that is executed after a :doc:`value-mapping-set` is applied successfully.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Mappings Applied Actions/Base Templates/Base Mappings Applied Action``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------
The base *mappings applied action* should not be used on 
its own. It is a base template for specific types of 
*mappings applied actions*.

All *mappings applied action* inherit the following fields:

.. |field-01| replace:: Rules
.. |description-01| replace:: The :doc:`mappings-applied-action-rule` that must pass in order for the *mappings applied action* to run. If no *mappings applied action rules* are specified, *mappings applied action* will always run.

+-------------------+-----------------------------+
| Field             | Description                 |
+===================+=============================+
| |field-01|        | |description-01|            |
+-------------------+-----------------------------+

.. seealso::
    
    For information on the *mappings applied actions* included 
    with the supported providers, see the section 
    :doc:`/component-reference/mappings-applied-actions/index` 
    in the :doc:`/component-reference/index`.

When to Extend
---------------------------------------------------
Data Exchange Framework comes with a set of standard 
*mappings applied actions*. In addition, each provider 
may include a set of *mappings applied actions* designed 
specifically for the system the provider integrates.

Custom *mappings applied actions* can be implemented 
in cases where special logic must be run after a 
*value mapping set* is applied successfully.

.. seealso::

    For information on how to implement a custom 
    *mappings applied action*, see the section 
    :doc:`/cookbooks/custom-components/custom-mappings-applied-action/index` 
    in the :doc:`/cookbooks/index`.
