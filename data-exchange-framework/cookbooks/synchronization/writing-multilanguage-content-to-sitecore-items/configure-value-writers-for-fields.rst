Configure Value Writers for Fields
=======================================

Now that your *pipeline* is configured to resolve a *target object* ,
you must configure the *value accessors* that are used to write values 
to the Sitecore item that is the *target object*.

1. In Content Editor, navigate to your tenant.
2. Navigate to **Data Access > Value Readers > Providers > Sitecore**.
3. Create (or select) an item based on the template :doc:`../../../components/sitecore/data-access/value-accessor-sets/item-fields`.
4. Select the *value accessor set* item.
5. Add (or select) an item based the template :doc:`../../../components/sitecore/data-access/value-accessors/item-field-value`.
6. Select the *value accessor* item.
7. Set the value of the field ``Language`` to the language you want to be able to write a value to.
8. Save the *value accessor* item.

.. hint::
    If your *pipeline* does not already contain a *pipeline step* 
    :doc:`../../../components/framework/pipeline-steps/apply-mapping`, 
    you must add and configure that *pipeline step*.