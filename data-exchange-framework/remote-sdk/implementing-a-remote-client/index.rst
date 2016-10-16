Implementing a Remote Client
=======================================

This section covers how to write a client application that uses
Data Exchange Framework Remote SDK. 

The client application can be anything: a console application, 
a web service, a mobile app, etc.

.. toctree::
    :name: implement-remote-client-steps
    :caption: Steps
    :maxdepth: 1 
    :titlesonly:

    configure-visual-studio-project
    test-connection
    list-tenants
    list-pipeline-batches
    run-pipeline-batch
    list-pipelines
    run-pipeline
    logging

.. important:: 

    The Sitecore server must have Sitecore Item Web API enabled. This
    means the following must be configured:

        * The Sitecore configuration setting **itemwebapi.mode** must be set to something other than ``Off``
        * SSL must be enabled on IIS

.. important::

    In the code samples in this section, you must make the following replacements:

    Replace **[SITECORE HOST]** with the host name of the Sitecore server
    you want to connect to. For example, ``sc82.localhost``.

    Replace **[SITECORE USER]** with your Sitecore user name, including
    the domain. For example, ``sitecore\\admin``.

    Replace **[SITECORE PASSWORD]** with the password for the Sitecore user.

    Replace **[DATABASE NAME]** with the name of the Sitecore database
    you want to read configuration from.

