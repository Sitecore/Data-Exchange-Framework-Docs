CRM Filter Expressions
======================================

Filter expressions are used to limit the data that is read from Dynamics CRM. 
These expressions are used to build the query for Dynamics CRM. As such, they 
reflect options that are available from the Dynamics CRM API.

.. note::
    These templates are defined in the following location:

    **Templates > Data Exchange > Providers > Dynamics CRM > Filter Expressions** 


.. note:: 

    It is important that you understand the implications of using 
    filter expressions before you configure them. These expressions 
    will change the data that is read from Dynamics CRM. You must 
    consider that data may not be read from Dynamics CRM may already 
    exist in Sitecore.
    
    Consider the example of synchronizing marketing list membership. 
    If you use a filter expression so that only contacts that have 
    changed in the past 24 hours, is that set of contacts going to 
    accurately reflect the marketing list membership?

.. toctree::
    :name: dynamics-crm-provider-filter-expressions-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    crm-expressions-base-attribute
    crm-expressions-boolean
    crm-expressions-date-range
    crm-expressions-numeric
    crm-expressions-relative-date
    crm-expressions-string
    crm-expressions-filter-expression
    