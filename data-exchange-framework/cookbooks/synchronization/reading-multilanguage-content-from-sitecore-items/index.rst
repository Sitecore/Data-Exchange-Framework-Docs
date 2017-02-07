Reading Multilanguage Content from Sitecore Items
====================================================================

When Sitecore items are involved in a synchronization process, it
may be necessary to use specific language versions of the Sitecore
items.

For example is where marketing campaign information in Sitecore 
is pushed to an external system. In Sitecore, the campaign information
is stored in Sitecore items. The campaign is used in a region where
English and French are used, so each campaign has content in those
languages. The external system is only able to handle the English
language content. 

This section covers how to read a field value from a specific language 
version of a Sitecore item. 

.. hint::
    This is needed when you want to use content from a specific language 
    as a *source object* in a synchronization process. This allows you
    to specify the language from which the content is read.

.. toctree::
    :name: sitecore-item-language-read
    :numbered:
    :titlesonly:

    configure-pipeline-to-read-sitecore-item-content
    specify-languages-to-read
    add-processor-to-resolve-language-versions-read
    configure-value-readers-for-fields
