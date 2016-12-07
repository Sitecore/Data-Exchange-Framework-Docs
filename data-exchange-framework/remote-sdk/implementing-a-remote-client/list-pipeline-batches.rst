List Pipeline Batches
=======================================

The approach used read a list of the *pipeline batches* for a *tenant*
is similar to the approach used to read the list of tenants. The only
difference is that you must specify the tenant whose pipeline batches
you want to read.

The following code demonstrates how you can list the pipeline batches 
that are configured on a specific tenant on the Sitecore server.

.. important:: 

    This code assumes the following namespaces are included by the ``using`` directive:

        * Sitecore.DataExchange.Remote.Http
        * Sitecore.DataExchange.Remote.Repositories
        * Sitecore.DataExchange.Repositories.Tenants

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
    // to read items from a Sitecore database. 
    var itemRepo = new WebApiItemModelRepository(DATABASE_NAME, cxSettings);
    //
    // Set the item model repository on the context so it is 
    // available to other framework components that need to
    // use it.
    Sitecore.DataExchange.Context.ItemModelRepository = itemRepo;
    //
    // Instantiate an object that uses the item repository to read
    // configuration items from the Sitecore server and convert
    // those items into Data Exchange Framework components.
    var repo = new SitecoreTenantRepository();
    //
    // Only read the tenant you are interested in.
    var tenant = repo.GetTenants().FirstOrDefault(t => t.Enabled && t.Name == "YOUR TENANT NAME");
    if (tenant == null)
    {
        //
        // The tenant you specified does not exist, or is not enabled.
        return;
    }
    //
    // Only read pipeline batches that are marked as being compatible with 
    // the remote API. This is a setting on the pipeline batch. 
    //
    // Whether or not a particular pipeline batch supports remote execution 
    // depends on the pipeline steps used in the pipeline. The remote API
    // Allows you to read all of the pipeline batches defined on a tenant.
    //
    // It is the responsibility of the client application to respect 
    // the setting that indicates whether or not a pipeline batch is 
    // compatible with the remote API.
    //
    // Likewise, it is the responsibility of the client application to 
    // respect the setting that indicates whether or not a pipeline 
    // batch is enabled.
    var batches = repo.GetPipelineBatches(tenant.ID, true).Where(b => b.Enabled);
    if (batches.Any())
    {
        //
        // At least one remote-compatible, active pipeline batch was returned.
    }
    else
    {
        //
        // No remote-compatible, active pipeline batches were returned.
    }