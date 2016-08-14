Remote SDK
=======================================

Data Exchange Framework Remote SDK allows *pipeline batches*, 
*pipelines* and other framework components to run outside of 
the Sitecore server. This can significantly reduce the load
on your Sitecore server by moving much I/O and other processing
to a separate machine.

When using the remote SDK, Sitecore's role in synchronization
processes is limited to configuration. Sitecore items are used
to configure framework components, but the framework components
themselves run within the application domain that is using the
remote SDK.

.. toctree::
    :caption: Topics
    :maxdepth: 1 
    :titlesonly:

    architecture
    implementing-a-remote-client/index

