Writing Multilanguage Content to Sitecore Items
====================================================================

When Sitecore items are involved in a synchronization process, it
may be necessary to use specific language versions of the Sitecore
items.

For example, consider a case where information is read from a PIM 
(product information system). Each product that is read from the PIM
has two descriptions: one in English and one in German. You want to
represent the product as a Sitecore item. The Sitecore template has
a single field used to store descriptions.

This section covers how to set a field value on a specific language 
version of a Sitecore item. 

.. hint::
    This is needed when you the *target object* in a synchronization 
    process is a Sitecore item, and you know which language you want
    to write values to on the Sitecore item.

.. toctree::
    :name: sitecore-item-language-write
    :numbered:
    :titlesonly:

    configure-pipeline-to-resolve-source
    specify-languages-to-write
    add-processor-to-resolve-language-versions-write
    configure-value-writers-for-fields
