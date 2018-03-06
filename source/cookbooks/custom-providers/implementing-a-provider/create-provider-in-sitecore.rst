Create Provider in Sitecore
===================================================
In Sitecore, a variety of templates and items must be 
created and configured for the provider. The Data 
Exchange Framework SDK automates much of this.

1. In Sitecore, open Content Editor.
2. Right-click on the ribbon and select **DATA EXCHANGE SDK**.

.. image:: _static/sdk-strip.png

3. Click **Data Exchange SDK**.

.. image:: _static/sdk-tab.png

4. Click **Create Provider**.

.. image:: _static/create-provider-button.png

5. Enter **File System** and click **OK**.

.. image:: _static/enter-provider-name.png

6. A progress box is displayed as the templates and items are created and configured.

.. image:: _static/creating-provider-dialog.png

7. The progress box will disappear after the provider is created. The following items were created in the Sitecore database:

    * ``/sitecore/templates/Branches/Data Exchange/Providers/File System``
    * ``/sitecore/templates/Data Exchange/Providers/File System``
    * ``/sitecore/system/Settings/Rules/Insert Options/Rules/Data Exchange - File System Provider``