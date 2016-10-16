Add Ability to Add Endpoints to Tenant
=======================================

*Endpoints* are configured on a *tenant*. Each tenant maintains its own
endpoints. Endpoints are not shared between tenants.

Under the tenant, endpoints are organized by *provider*. Each provider 
has its own folder. In this folder are all of the endpoints that are
based on endpoints included with the provider.

The following screenshot shows a tenant from a Sitecore server with
two providers installed: one for Dynamics CRM and one for Sitecore.
Notice that the endpoints for each provider are organized under a
folder whose name matches the name of the provider. These are called
*endpoint items folders*.

    .. image:: _static/endpoint-folders.png

Add template for endpoint items folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A new template is needed to represent the folder used to store 
endpoints for the file system provider.

1. In Sitecore, open Template Manager.
2. Navigate to **Templates > Data Exchange > Providers > File System**.
3. Add a template folder named **Folders**.
4. Add the following template:

    +-------------------+---------------------------------------------------------------------+
    | Name              | | **File System Endpoints Root**                                    |
    +-------------------+---------------------------------------------------------------------+
    | Base template     | | **Templates > Data Exchange > Framework > Folders >**             |
    |                   | | **Folders for Endpoints > Base Endpoints for Provider Root**      |
    +-------------------+---------------------------------------------------------------------+
    | Location          | | **Templates > Data Exchange > Providers > File System > Folders** |
    +-------------------+---------------------------------------------------------------------+

5. Note the id for this template, because you will need it later.
6. Set the icon for this template to ``Office/32x32/folder_open.png``.

Add insert option for adding endpoint items to folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Adding an insert option to the folder where endpoint items are stored 
makes it easier for people to add new endpoint items.

1. Add the Standard Values item.
2. Navigate to the Standard Values item.
3. In the Insert Options, assign the template **Templates > Data Exchange > Providers > File System > Endpoints > Text File Endpoint**.

Add command template for endpoint items folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In the following screenshot, you can see that the endpoints for 
each provider are organized in folders. The name of each folder
corresponds with the name of the provider.

For example, the endpoints for the Dynamics CRM provider are 
organized under a folder named **Dynamics CRM**.

    .. image:: _static/endpoint-folders.png

Normally when Sitecore items are created, the user creating the
item specifies the name of the item. In this case, however, you
do not want to count on the user getting this right. Instead,
you want to ensure the item name matches the name of the provider:
**File System**.

This is accomplished using a Sitecore *command template*.

    .. hint:: 
    
        The idea of providers is that a system may already have Data 
        Exchange Framework set up with tenants already configured.
        The person installing your provider will want to be able to
        incorporate your provider into their existing tenant.

        However, you do not want to force anyone to use your provider.
        Let the person who wants to use your provider determine when
        and where to use the provider. This means you should not 
        automatically make any changes to the existing tenants. 
        
        For example, when your provider is installed, you should not
        automatically create a new **File System** folder in the 
        existing tenants. Instead, make it as easy as possible for
        the person who is responsible for configuring the tenants 
        to discover and use your provider. This is what most of 
        this section is describing how to do.

1. In Template Manager, navigate to **Templates > Branches > Data Exchange > Providers**.
2. Add a branch folder named **File System**.
3. Navigate to **Templates > Branches > Data Exchange > Providers > File System**.
4. Add a branch folder named **Commands**.
5. Navigate to **Templates > Branches > Data Exchange > Providers > File System > Commands**.
6. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Create Item Without Prompting for Name Branch**                   |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **File System Endpoints Root**                                      |
    +-------------------+---------------------------------------------------------------------+

    .. note:: 
    
        The template **Create Item Without Prompting for Name Branch** is 
        included with Data Exchange Framework. It, itself, is a command
        template.

7. Navigate to **Templates > Branches > Data Exchange > Providers > File System > Commands > File System Endpoints Root > New Item Settings**.

    .. note:: 

        The command template uses this item to determine what kind of 
        item to create, and the name of the item.

8. Set the following field values:

    +-----------------------+---------------------------------------------------------------------+
    | Field                 | Value                                                               |
    +=======================+=====================================================================+
    | Name for new item     | | **File System**                                                   |
    +-----------------------+---------------------------------------------------------------------+
    | Template for new item | | **Templates > Data Exchange > Providers > File System >**         |
    |                       | | **Folders > File System Endpoints Root**                          |
    +-----------------------+---------------------------------------------------------------------+

Add insert option for command template
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You have created a command template that can create an endpoint items 
folder where the item name is always **File System**. But where is
this command template ever used?

The endpoint items folder must be added to a folder that organizes 
the endpoint items folders for all of the providers that are 
available to the tenant.

In the following screenshot, that folder is **Data Exchange > mycrm > Endpoints > Providers**.
Notice that under this folder are folders for **Dynamics CRM** and **Sitecore**.
This indicates that there are two providers available for the tenant **mycrm**.

    .. image:: _static/endpoint-folders.png

.. note:: 

    Adding this insert option is a little more complex. For each 
    tenant there should only be one endpoint items folder for the 
    file system provider. All of the endpoint items go in this one 
    folder.
    
    This means the insert option for the endpoints folder will only 
    appear under a specific condition: no endpoints folder item has 
    already been added. *Insert option rules* support the ability 
    to define this condition.  

1. Open Content Editor.
2. Navigate to **sitecore > system > Settings > Rules > Insert Options > Rules**.
3. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Insert Option Rule**                                              |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **Data Exchange - File System Provider**                            |
    +-------------------+---------------------------------------------------------------------+

4. Set the following field values:

    +-------------------+---------------------------------------------------------------------------------------------+
    | Field             | Value                                                                                       |
    +===================+=============================================================================================+
    | Name              | **Add insert options for the File System provider for the Data Exchange Framework**         |
    +-------------------+---------------------------------------------------------------------------------------------+

5. On the field **Rule**, click **Edit rule**.
6. Add the action **add specific insert option**.
7. This action requires you specify a template. Select **Branches > Data Exchange > Providers > File System > Commands > File System Endpoints Root**.
8. Add the condition **where the item template is specific template**.
9. This condition requires you specify a template. Select **Data Exchange > Framework > Folders > Folders for Endpoints > Endpoints Providers Root**.
10. Add another condition. Add the condition **where the result of the expression query exists**.
11. This condition requires you specify an expression. Enter ``./*[@@templateid='TEMPLATE-ID']``,  
    being careful to replace  ``TEMPLATE-ID`` with the id from the template you created named **Text File Endpoint**.

    .. hint:: 

        The purpose of this condition is to reduce the chances that 
        more than one folder for file system endpoints is created. 
        
        However, insert options are not fool-proof. New items of 
        any type can still be created using the **Insert from template** 
        option available in Content Editor.

12. Negate the condition by clicking **where**.

    .. note:: 
    
        Negating the condition changes **where** to **except where**.

13. Name the rule **Endpoints Providers Root**.

    .. image:: _static/endpoints-folder-rule.png

14. Click **OK** to save the rule.
15. Save the Sitecore item.

Test the configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following steps explain how to confirm your configuration 
is working properly.

1. In Content Editor, navigate to **sitecore > system > Data Exchange**.
2. Select a tenant.
3. Under the tenant, navigate to **Endpoints > Providers**.

In the insert options, the option to insert **File System Endpoints Root** is available.

    .. image:: _static/insert-option-available.png

4. Use the insert option to create a new item.

A new item named **File System** is created. The insert option for the endpoint item is available.

    .. image:: _static/endpoint-insert-option-available.png

If you navigate back to the **Providers** item, the insert option for **File System Endpoints Root** 
is no longer available.

    .. image:: _static/insert-option-unavailable.png

5. Delete the item **File System**.

Once again, in the insert options, the option to insert **File System Endpoints Root** is available.

    .. image:: _static/insert-option-available.png
