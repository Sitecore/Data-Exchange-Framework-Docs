Add Ability to Add Pipeline Steps to Pipeline
=================================================

*Pipeline steps* are configured on a *pipeline*. Each pipeline maintains 
its own pipeline steps. Pipeline steps are not shared between pipelines.
Each tenant maintains its own pipelines. Pipelines are not shared 
between tenants.

The purpose of a pipeline is to model a process. It is possible that
a single pipeline may use pipeline steps from a number of different
*providers*. 

For example, one pipeline step may read data from CRM and another pipeline 
step may map that data to Sitecore. This process involves pipeline steps
from two different providers: the CRM provider and the Sitecore provider.

Insert options are used to inform the person configuring a pipeline
about which pipeline steps are available to be used. 

    .. note:: 
    
        An *insert option rule* is used to add the insert option. The 
        reason for this is because insert option rules allow you to
        configure an insert option without modifying the template
        you are adding the insert option to. 
        
        If every developer who creates a custom pipeline step were to 
        add an insert option directly to the pipeline template, one
        developer could very easily overwrite the insert option added
        by another developer. Insert option rules avoid this problem
        completely.  


Add insert option for pipelines
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Open Content Editor.
2. Navigate to **sitecore > system > Settings > Rules > Insert Options > Rules > Data Exchange - File System Provider**.
3. On the field **Rule**, click **Edit rule**.
4. Click **Add a new rule**.
5. Add the action **add specific insert option**.
6. This action requires you specify a template. Select **Data Exchange > Providers > File System > Pipeline Steps > Read Text File Pipeline Step**.
7. Add the condition **where the item template is specific template**.
8. This condition requires you specify a template. Select **Data Exchange > Framework > Pipelines > Pipeline**.
9. Name the rule **Pipelines**.

    .. image:: _static/pipelines-rule.png

10. Click **OK** to save the rule.
11. Save the Sitecore item.

Test the configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following steps explain how to confirm your configuration 
is working properly.

1. In Content Editor, navigate to **sitecore > system > Data Exchange**.
2. Select a tenant.
3. Under the tenant, navigate to **Pipelines**.
4. Select a pipeline.

In the insert options, the option to insert **Read Text File Pipeline Step** is available.

    .. image:: _static/pipeline-step-available.png

