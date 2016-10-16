Use the Provider
=======================================

This section covers how to configure a *pipeline batch* that uses the
file system provider to create and populate Sitecore items from the 
contents of a text file.

For this example, you will create a file that contains information about 
different cities. Each row in the file represents a single city. Each
city will be represented in Sitecore as an item. 

The synchronization process will read the cities from the file and 
create Sitecore items for each. If a Sitecore item already exists
for a city in the file, the Sitecore item will be updated with the
information from the file. 

.. toctree::
    :name: use-the-provider-steps
    :caption: Steps
    :maxdepth: 1
    :titlesonly:

    create-source-file
    add-tenant
    add-endpoint-for-source
    add-value-accessor-set-for-source
    create-template-for-target
    add-folder-to-hold-new-sitecore-items
    add-endpoint-for-target
    add-value-accessor-set-for-target
    add-value-mapping-set
    add-pipeline-to-sync-single-record-from-source
    add-pipeline-step-to-resolve-target-item
    add-pipeline-step-to-apply-mapping
    add-pipeline-step-to-update-sitecore-item
    add-pipeline-to-read-source
    add-pipeline-step-to-read-from-source
    add-pipeline-step-to-iterate-data-from-source
    add-pipeline-batch
    test-pipeline-batch



