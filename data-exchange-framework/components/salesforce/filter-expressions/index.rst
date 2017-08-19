Filter Expressions
======================================

Filter expressions are used to limit the data that is read from Salesforce. 
These expressions are used to build the query for Salesforce. As such, they 
reflect options that are available from the Salesforce API.

.. note::
    These templates are defined in the following location:

    **Templates > Data Exchange > Providers > Salesforce > Filter Expressions** 

.. note:: 

    It is important that you understand the implications of using 
    filter expressions before you configure them. These expressions 
    will change the data that is read from Salesforce. You must 
    consider that data may not be read from Salesforce may already 
    exist in Sitecore.
    
.. toctree::
    :name: salesforce-provider-filter-expressions-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    salesforce-expressions-filter-expression
    salesforce-expressions-boolean
    salesforce-expressions-date-range
    salesforce-expressions-null
    salesforce-expressions-numeric
    salesforce-expressions-relative-date
    salesforce-expressions-string
    