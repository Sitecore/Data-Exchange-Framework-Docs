Apply Mapping Rules
=======================

An *apply mapping rule* is used to configure a condition that must 
be met in order for a *value mapping* to be applied.

For example, consider a case where you are storing customer information
in CRM and in Sitecore. It is possible that a value, like the customer's
birthday, is stored in both systems.

A value mapping is used to ensure the CRM value overwrites the Sitecore
value. But what if, in CRM, the customer has no birthday day, while in
Sitecore, the customer does?

Using a value mapping, the value from CRM will overwrite the value in
Sitecore, which means that data in Sitecore will be lost.

Apply mapping rules can be used in this situation to prevent the value
mapping from being used if the CRM value is not set.

.. note::
    These templates are defined in the following location:

    **Templates > Data Exchange > Framework > Data Access > Apply Mapping Rules** 

.. toctree::
    :name: framework-apply-mapping-rule-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    collection-count-mapping-rule
    default-value-mapping-rule
    null-value-mapping-rule
    objects-are-different-mapping-rule
    
.. toctree::
    :name: framework-apply-mapping-rule-base-templates
    :caption: Base Templates 
    :titlesonly:
    :maxdepth: 2

    base-apply-mapping-rule
