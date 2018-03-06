Use the Provider
===================================================
This section covers how to configure a pipeline batch 
that uses the file system provider to create and populate 
Sitecore items from the contents of a text file.

For this example, you will create a file that contains 
information about different cities. Each row in the file 
represents a single city. Each city will be represented 
in Sitecore as an item.

The synchronization process will read the cities from the 
file and create Sitecore items for each. If a Sitecore item 
already exists for a city in the file, the Sitecore item 
will be updated with the information from the file.

.. note::

    This example assumes you have the Sitecore Provider 
    for Data Exchange Framework installed. This provider
    is available for download on the 
    `Sitecore Developer Portal <https://dev.sitecore.net/Downloads/Data_Exchange_Framework.aspx>`_.

.. toctree::
   :maxdepth: 1

   create-source-file.rst
   add-tenant.rst
   add-endpoint-for-source-file.rst
   add-value-accessors-for-source-file.rst
   create-template-for-target-items.rst
   add-parent-item-for-target-items.rst
   add-endpoint-for-target-items.rst
   add-value-accessors-for-target-items.rst
   add-value-mappings.rst
   add-pipeline-to-sync-single-row-from-source-file.rst
   add-pipeline-step-to-resolve-target-item.rst
   add-pipeline-step-to-apply-mappings.rst
   add-pipeline-step-to-update-target-item.rst
   add-pipeline-to-read-source-file.rst
   add-pipeline-step-to-read-data-from-source-file.rst
   add-pipeline-step-to-iterate-data-read-from-source-file.rst
   add-pipeline-batch.rst
   test-pipeline-batch.rst