Apply Mappings Pipeline Step
===================================================

.. |component-description| replace:: The *apply mappings pipeline step* is a component that handles the logic required to apply a :doc:`value-mapping-set`.
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Pipeline Steps/Apply Mapping Pipeline Step``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------

.. |field-01| replace:: Mapping Set
.. |description-01| replace:: The *value mapping set* that is applied when the pipeline step runs.
.. |field-02| replace:: Actions
.. |description-02| replace:: If the *value mapping set* is applied successfully, the specified :doc:`Mappings Applied Rules <mappings-applied-action>` run afterwards. 
.. |field-03| replace:: Source Object Location
.. |description-03| replace:: When a *value mapping set* is applied, data is read from the object at this location.
.. |field-04| replace:: Target Object Location
.. |description-04| replace:: When a *value mapping set* is applied, data is written to the object at this location.

+-------------------+-----------------------------+
| Field             | Description                 |
+===================+=============================+
| |field-01|        | |description-01|            |
+-------------------+-----------------------------+
| |field-02|        | |description-02|            |
+-------------------+-----------------------------+
| |field-03|        | |description-03|            |
+-------------------+-----------------------------+
| |field-04|        | |description-04|            |
+-------------------+-----------------------------+

When to Extend
---------------------------------------------------
It is unusual to need to extend this component.