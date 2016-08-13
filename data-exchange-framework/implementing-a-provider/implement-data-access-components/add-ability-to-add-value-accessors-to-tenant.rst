Add Ability to Add Value Accessors to Tenant
=================================================

*Value accessor sets* are configured on a *tenant*. Each tenant maintains 
its own value accessor sets. Value accessor sets are not shared between 
tenants.

Under the tenant, value accessor are organized by *provider*. Each provider 
has its own folder. In this folder are all of the value accessor sets that 
are based on value accessor sets that are relevant for the provider.

    .. hint:: 

        The steps in this section follow the pattern established in the
        section that covers implementing an endpoint. Since that section
        goes into detail on the reasons and benefits of this approach,
        that information will not be duplicated here.

Add template for value accessor set items folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A new template is needed to represent the folder used to store 
value accessor sets for the file system provider.

1. In Sitecore, open Template Manager.
2. Navigate to **Templates > Data Exchange > Providers > File System > Folders**.
3. Add the following template:

    +-------------------+---------------------------------------------------------------------+
    | Name              | | **File System Value Accessor Sets Root**                          |
    +-------------------+---------------------------------------------------------------------+
    | Base template     | | **Templates > Data Exchange > Framework > Folders >**             |
    |                   | | **Folders for Data Access > Value Accessor Sets for**             |
    |                   | | **Provider Root**                                                 |
    +-------------------+---------------------------------------------------------------------+
    | Location          | | **Templates > Data Exchange > Providers > File System > Folders** |
    +-------------------+---------------------------------------------------------------------+

4. Note the id for this template, because you will need it later.
5. Set the icon for this template to ``Office/32x32/folder_open.png``.

Add insert option for adding value accessor set items to folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Adding an insert option to the folder where value accessor set items 
are stored makes it easier for people to add new value accessor set 
items.

1. Add the Standard Values item.
2. Navigate to the Standard Values item.
3. In the Insert Options, assign the template **Templates > Data Exchange > Providers > File System > Data Access > Array Value Accessor Set**.
4. In the Insert Options, remove the template **Templates > Data Exchange > Framework > Data Access > Value Accessors > Value Accessor Set**. 

    .. note:: 
    
        The default value accessor set template is removed in order to 
        reduce complexity for the person configuring the value accessor 
        set. 

        When using the provider, there is no reason to use the default
        value accessor set. The custom value accessor set should be used.

Add command template for value accessor set items folder
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A command template ensures the folder used to organize the value accessor
set items has a name that is consistent with other framework components.

1. In Template Manager, navigate to **Templates > Branches > Data Exchange > Providers > File System > Commands**.
2. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Create Item Without Prompting for Name Branch**                   |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **File System Value Accessor Sets Root**                            |
    +-------------------+---------------------------------------------------------------------+

3. Navigate to **Templates > Branches > Data Exchange > Providers > File System > Commands > File System Value Accessor Sets Root > New Item Settings**.
4. Set the following field values:

    +-----------------------+---------------------------------------------------------------------+
    | Field                 | Value                                                               |
    +=======================+=====================================================================+
    | Name for new item     | | **File System**                                                   |
    +-----------------------+---------------------------------------------------------------------+
    | Template for new item | | **Templates > Data Exchange > Providers > File System >**         |
    |                       | | **Folders > File System Value Accessor Sets Root**                |
    +-----------------------+---------------------------------------------------------------------+

Add insert option for command template
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The insert option will allow users to add one, and only one, folder
for organizing value accessor set items for the provider, per tenant.

1. Open Content Editor.
2. Navigate to **sitecore > system > Settings > Rules > Insert Options > Rules > Data Exchange - File System provider**.
3. On the field **Rule**, click **Edit rule**.
4. Click **Add a new rule**.
5. Add the action **add specific insert option**.
6. This action requires you specify a template. Select **Branched > Data Exchange > Providers > File System > Commands > File System Value Accessor Sets Root**.
7. Add the condition **where the item template is specific template**.
8. This condition requires you specify a template. Select **Data Exchange > Framework > Folders > Folders for Data Access > Value Accessor Sets Providers Root**.
9. Add another condition. Add the condition **where the result of the expression query exists**.
10. This condition requires you specify an expression. Enter ``./*[@@templateid='TEMPLATE-ID']``, being careful to replace  **TEMPLATE-ID** with the id from the template you created.
11. Negate the condition by clicking **where**.

    .. note:: 
    
        Negating the condition changes **where** to **except where**.

12. Name the rule **Value Accessor Sets Providers Root**.

    .. image:: _static/value-accessor-sets-folder-rule.png

13. Click **OK** to save the rule.
14. Save the Sitecore item.

Test the Configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following steps explain how to confirm your configuration 
is working properly.

1. In Content Editor, navigate to **sitecore > system > Data Exchange**.
2. Select a tenant.
3. Under the tenant, navigate to **Data Access > Value Accessor Sets > Providers**.

In the insert options, the option to insert **File System Value Accessor Sets Root** is available.

    .. image:: _static/insert-option-available.png

4. Use the insert option to create a new item.

A new item named **File System** is created. The insert option for the endpoint item is available.

    .. image:: _static/value-accessor-set-insert-option-available.png

If you navigate back to the **Providers** item, the insert option for **File System Value Accessor Sets Root** 
is no longer available.

    .. image:: _static/insert-option-unavailable.png

5. Delete the item **File System**.

Once again, in the insert options, the option to insert **File System Value Accessor Sets Root** is available.

    .. image:: _static/insert-option-available.png
