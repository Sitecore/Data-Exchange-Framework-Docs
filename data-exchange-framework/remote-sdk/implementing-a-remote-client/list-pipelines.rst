List Pipelines
=======================================

The approach used read a list of the *pipelines* for a *tenant*
is similar to the approach used to read the list of *pipeline batches*
in that you must specify the tenant whose pipelines you want to read.

But it is different in the way you go about finding the pipelines.
When reading pipeline batches, a *pipeline batch repository* is used.
This repository has a method that returns the pipeline batches for
the specified tenant. There is no such method for reading the pipelines
for a tenant.

A different approach is used. This approach can be used to read any
framework component.

.. warning::

    Using this code is risky because it may return pipelines that
    are not compatible with the remote SDK. A safer approach is to
    get the pipeline batches that are compatible with the remote
    SDK and then iterate those pipelines.

The following code demonstrates how you can list the pipelines 
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
    //
    var pipelines = repo.GetPipelines(tenant.ID, true).Where(b => b.Enabled);
    if (pipelines.Any())
    {
        //
        // At least one enabled pipeline was returned.
    }
    else
    {
        //
        // No pipelines were returned. 
    }
