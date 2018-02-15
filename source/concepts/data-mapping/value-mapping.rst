Value Mapping
===================================================

.. |component-description| replace:: A *value mapping* controls the mapping of a single value from one object to another. 
.. |template-location| replace:: ``/sitecore/templates/Data Exchange/Framework/Data Access/Mapping/Value Mapping``

+-------------------+-----------------------------+
| Description       | |component-description|     |
+-------------------+-----------------------------+
| Template location | |template-location|         |
+-------------------+-----------------------------+

.. contents:: In this topic:
   :local:

Configuration
---------------------------------------------------

.. |field-01| replace:: Source Accessor
.. |description-01| raw:: html
   
   <a href="value-accessor.html">Value Accessor</a> used to read the values to be mapped from the <i>source object</i>. (More precisely, the <i>value reader</i> assigned to the <i>value accessor</i> is used.)
   
   If multiple <i>value accessors</i> are specified, the value read from the <i>source object</i> are added to a collection. This is used when the <i>value writer</i> expects multiple values (such as when the value writer represents a method).

.. |field-02| replace:: Always Read Values Into Collection
.. |description-02| raw:: html

    When ticked, even if only one source value accessor is specified, a collection is read (meaning a new collection is created and the value read by is added to the collection). 

    This option is used when the <i>value writer</i> expects a collection of values (such as when the value writer represents a method).

.. |field-03| replace:: Target Accessor
.. |description-03| replace:: :doc:`value-accessor` used to write the value to be mapped to the target object. (More precisely, the *value writer* assigned to the *value accessor* is used.)

.. |field-04| replace:: Source Value Pre Transformer
.. |description-04| raw:: html

    <a href="value-reader.html">Value Reader</a> used to convert the <i>source object</i> before the <i>source accessor</i> is used. The converted value becomes the <i>source object</i> within the context of this <i>value mapping</i>.

    This option is used when the <i>source object</i> must be converted into a different format before the <i>source accessor</i> can be used to read a value from it.

.. |field-05| replace:: Source Value Transformer
.. |description-05| raw:: html

    <a href="value-reader.html">Value Reader</a> used convert the value read by the <i>source accessor</i> before the value is written to the <i>target object</i>.

    This option is used when the value read from the <i>source object</i> must be converted into a different format before the <i>target  accessor</i> can be used to write the value to the <i>target object</i>.

.. |field-06| replace:: Do Not Fail If Unable To Read Source Value
.. |description-06| replace:: By default, the a value cannot be read from the *source object*, this is considered a failure in the data mapping process. When ticked, the *value mapping* does not fail, it simply does not run.

.. |field-07| replace:: Ignore Null Values
.. |description-07| replace:: By default, if a null value is read from the *source object*, the *value mapping* does not run. This prevents existing data from being overwritten. When unticked, the *value mapping* runs even if a null value is read from the *source object*.

.. |field-08| replace:: Apply Mapping Rules
.. |description-08| raw:: html

    <a href="apply-mapping-rule.html">Apply Mapping Rules</a> that determine whether the <i>value mapping</i> should run. 
    
    When specified, all <i>apply mapping rules</i> must pass in order for the <i>value mapping</i> to run. If one <i>apply mapping rule</i> fails, the <i>value mapping</i> does not run.

.. |field-09| replace:: Mapping Set Fails If This Mapping Fails
.. |description-09| raw:: html

    By default, when a single <i>value mapping</i> fails, this does not result in the entire mapping process from failing. When ticked, if this <i>value mapping</i> fails, the entire mapping process fails.

    This option is used when the <i>value mapping</i> is critical to the data mapping process. For example, if the <i>value mapping</i> is the way a primary key is set on the <i>target object</i>, it will not be possible to update the target system. This is a critical error, so the mapping process should fail.

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
| |field-05|        | |description-05|            |
+-------------------+-----------------------------+
| |field-06|        | |description-06|            |
+-------------------+-----------------------------+
| |field-07|        | |description-07|            |
+-------------------+-----------------------------+
| |field-08|        | |description-08|            |
+-------------------+-----------------------------+
| |field-09|        | |description-09|            |
+-------------------+-----------------------------+

When to Extend
---------------------------------------------------
It is unusual to need to extend this component.
