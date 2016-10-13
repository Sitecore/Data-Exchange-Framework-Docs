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

.. note::
    Source code for this example is available on 
    `GitHub <https://github.com/Sitecore/Sitecore.DataExchange.Examples>`_.

.. hint:: 

    API documentation is available on the `Sitecore Developer Portal <https://dev.sitecore.net/Downloads/Dynamics_CRM_Connect/Dynamics_CRM_Connect_1/Dynamics_CRM_Connect_11.aspx>`_.

.. toctree::
    :name: topics-remote-sdk
    :caption: Topics
    :maxdepth: 1 
    :titlesonly:

    architecture
    implementing-a-remote-client/index

