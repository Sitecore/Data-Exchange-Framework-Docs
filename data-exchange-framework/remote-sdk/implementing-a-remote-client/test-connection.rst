Test Connection
=======================================

When using Data Exchange Framework Remote SDK, you read configuration
settings from the Sitecore server. Therefore, it is important that you
are able to establish a connection to the Sitecore server. 

The following code demonstrates how you can test the connection to 
the Sitecore server.

.. important:: 

    This code assumes the following namespaces are included by the ``using`` directive:

        * Sitecore.DataExchange.Remote.Http
        * Sitecore.DataExchange.Remote.Repositories

.. code-block:: c#

    //
    // Specify the settings used to make a connection.
    var cxSettings = new ConnectionSettings
    {
        Host = HOST_NAME,
        UserName = USER_NAME,
        Password = PASSWORD,
    };
    //
    // Instantiate an object that uses the Sitecore item web API 
    // to read items from a Sitecore database. This functionality
    // enables you to determine whether or not a connection can
    // be established with the Sitecore server.
    var itemRepo = new WebApiItemModelRepository(DATABASE_NAME, cxSettings);
    //
    // Get the item specified by the parameter.
    var item = itemRepo.Get("/sitecore/content/Home");
    if (item != null)
    {
        //
        // A connection was established with the Sitecore server
        // and the specified item was found.
    }
    else
    {
        //
        // The item was not found, but a connection was still 
        // established with the Sitecore server.
    }
