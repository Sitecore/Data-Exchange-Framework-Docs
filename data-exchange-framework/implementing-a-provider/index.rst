Implementing a Provider
=======================================

This section walks you through the process of creating a   
provider for Data Exchange Framework that is able to read 
data from a text file, such as a file that contains 
comma-separated values (CSV). 

.. note::
    Source code and a Sitecore package that contains the  
    finished solution for this example is available on 
    `GitHub <https://github.com/Sitecore/Sitecore.DataExchange.Examples>`_.

.. important::
    Before following these instructions, be sure to download and 
    install for `hotfix 128342 <https://dev.sitecore.net/Downloads/Data_Exchange_Framework/1x/Data_Exchange_Framework_11.aspx>`_
    Sitecore Provider for Data Exchange Framework 1.1.

    This hotfix resolves some issues that prevent certain components
    from being properly configured on empty tenants. 

.. toctree::
    :name: steps-implementing-a-provider
    :caption: Steps
    :numbered:
    :maxdepth: 1
    :titlesonly:

    define-requirements
    create-visual-studio-project
    add-template-folder-for-provider
    implement-endpoint/index
    implement-pipeline-step/index
    implement-data-access-components/index
    use-the-provider/index

