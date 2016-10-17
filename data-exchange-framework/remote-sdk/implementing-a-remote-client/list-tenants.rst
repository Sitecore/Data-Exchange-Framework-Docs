List Tenants
=======================================

A *tenant* is the main unit of configuration in Data Exchange Framework.
Pretty much anything you can do with Data Exchange Framework requires you
first identify a tenant.

The following code demonstrates how you can list the tenants that are
configured on the Sitecore server.

.. important:: 

    This code assumes the following namespaces are included by the ``using`` directive:

        * Sitecore.DataExchange.Models
        * Sitecore.DataExchange.Remote.Http
        * Sitecore.DataExchange.Remote.Repositories
        * Sitecore.DataExchange.Repositories.PipelineBatches

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
    // Instantiate an object that uses the item repository to read
    // configuration items from the Sitecore server and convert
    // those items into Data Exchange Framework components.
    var repo = new SitecorePipelineBatchRepository
    {
        ItemModelRepository = itemRepo
    };
    //
    // Only read enabled tenants. The remote API allows you to read
    // all of the tenants defined on a Sitecore server. It is the 
    // responsibility of the client application to respect the 
    // setting that indicates whether or not a tenant is enabled.
    var tenants = repo.GetTenants().Where(t => t.Enabled);
    if (tenants.Any())
    {
        //
        // At least one enabled tenant was returned.
    }
    else
    {
        //
        // No tenants were returned. Since no exception was thrown,
        // it is likely the Sitecore server either has no tenants
        // defined on it, or none of the tenants are enabled.
    }
