Run Pipeline Batch
=======================================

A *pipeline batch* is designed to run asynchronously, usually to 
synchronize multiple records at once.

The following code demonstrates how you can list the pipeline batches 
that are configured on a specific tenant on the Sitecore server.

.. important:: 

    This code assumes the following namespaces are included by the ``using`` directive:

        * Sitecore.DataExchange.Remote.Http
        * Sitecore.DataExchange.Remote.Repositories
        * Sitecore.DataExchange.Remote.Runners
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
    // Only read the tenant you are interested in.
    var tenant = repo.GetTenants().FirstOrDefault(t => t.Enabled && t.Name == "YOUR TENANT NAME");
    if (tenant == null)
    {
        //
        // The tenant you specified does not exist, or is not enabled.
        return;
    }
    //
    // Only read the pipeline batch you are interested in.
    var batches = repo.GetPipelineBatches(tenant.ID, true);
    var batch = batches.FirstOrDefault(b => b.Enabled && b.Name == "YOUR BATCH NAME");
    if (batch == null)
    {
        //
        // The pipeline batch you specified does not exist, or is not enabled.
        return;
    }
    //
    // Instantiate an object that runs pipeline batches.
    var runner = new RemotePipelineBatchRunner();
    if (!runner.Run(batch))
    {
        //
        // The runner was not started or an error occurred and the 
        // pipeline batch was aborted.
        return;
    }

.. note:: 

    After this code runs, if you check the Sitecore item that represents 
    the pipeline batch you will see that fields in the **Summary** 
    section are populated.