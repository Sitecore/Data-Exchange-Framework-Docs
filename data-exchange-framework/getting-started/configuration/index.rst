Configuration
=======================================

Data Exchange Framework uses Sitecore items to configure 
synchronization processes. 

It is important to note that while a synchronization process
is configured using Sitecore items, that does not mean the 
synchronization process must run on the Sitecore server. In
fact, Data Exchange Framework was designed so that the 
synchronization process can run outside of the Sitecore server.

Data Exchange Framework includes components that are responsible
for reading the configuration from Sitecore and converting that
configuration into components from the framework, such as *pipelines*,
*pipeline steps*, *value readers*, etc.    

Configuration involves the following components: 

.. toctree::
    :maxdepth: 2
    :titlesonly:

    converter
    item-model-repository
    pipeline-batch-repository
    plugin
    provider
    tenant