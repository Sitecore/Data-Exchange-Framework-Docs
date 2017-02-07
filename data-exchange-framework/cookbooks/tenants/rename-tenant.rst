Rename a Tenant
=======================

Within xDB, certain contact facets support multiple values. For example, 
a contact may have multiple email addresses. Each of these email addresses 
has an identifier or name associated with it, such as **work** or **home**.

By default, when these sorts of values are read from the CRM, the name of 
the tenant is used as the identifier. If the name of the tenant is **mycrm**, 
when you synchronize a CRM contact, the email address that is read from the 
CRM will be the **mycrm** email address.

1.	In Content Editor, navigate to the tenant you want to rename.
2.	Rename the Sitecore item.
3.	Navigate to **Data Access > Value Readers > Providers > Dynamics CRM > Constant Value Reader - Tenant Name**.
4.	In the field **Value**, enter the new tenant name.
5.	Save the item.
6.	Navigate to **Data Access > Value Accessor Sets > Providers > Sitecore > xDB Contact Properties**.
7.	For each item that uses the template 
        **xDB Contact Facet Indexer Property Value Accessor**, change  
        the value of the property **Index name for indexer property** 
        to match the new tenant name.

.. note:: 

    Renaming a tenant will not change data that already exists in xDB. 
    The next time data is synchronized, the new tenant name will be 
    used. However, this may result in duplicate data in xDB.

    For example, if you have already run the contact synchronization 
    process and the tenant name is **mycrm**, you will have an email 
    address identified as the **mycrm** email address. If you rename 
    the tenant to **Production CRM** and run the process again, you 
    will now have an email address identified as the **Production CRM** 
    email address. The **mycrm** email address will remain.
