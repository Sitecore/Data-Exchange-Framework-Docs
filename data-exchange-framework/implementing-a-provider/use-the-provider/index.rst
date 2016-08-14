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
    :caption: Steps
    :numbered:
    :maxdepth: 1
    :titlesonly:

    create-source-file.rst
    add-tenant.rst
    add-endpoint-for-source.rst
    add-value-accessor-set-for-source.rst
    create-template-for-target.rst
    add-folder-to-hold-new-sitecore-items.rst
    add-endpoint-for-target.rst
    add-value-accessor-set-for-target.rst
    add-value-mapping-set.rst
    add-pipeline-to-sync-single-record-from-source.rst
    add-pipeline-step-to-resolve-target-item.rst
    add-pipeline-step-to-apply-mapping.rst
    add-pipeline-step-to-update-sitecore-item.rst
    add-pipeline-to-read-source.rst
    add-pipeline-step-to-read-from-source.rst
    add-pipeline-step-to-iterate-data-from-source.rst
    add-pipeline-batch.rst
    test-pipeline-batch.rst



