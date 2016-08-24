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

.. note:: 

    In the future version of Data Exchange Framework, a repository
    will be available that will make it easier to access pipelines.

    However, in most cases, if you need to run a specific pipeline,
    you will know which pipeline you need. The process for resolving
    a pipeline if you have the item ID for the pipeline item is much
    simpler than the process below.

The following code demonstrates how you can list the pipelines 
that are configured on a specific tenant on the Sitecore server.

.. important:: 

    This code assumes the following namespaces are included by the ``using`` directive:

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
    // Set the item model repository on the context so it is 
    // available to other framework components that need to
    // use it.
    Sitecore.DataExchange.Context.ItemModelRepository = itemRepo;
    //
    // Instantiate an object that uses the item repository to read
    // configuration items from the Sitecore server and convert
    // those items into Data Exchange Framework components.
    var repo = new SitecorePipelineBatchRepository();
    //
    // Only read the tenant you are interested in.
    var tenant = repo.GetTentants().FirstOrDefault(t => t.Enabled && t.Name == "YOUR TENANT NAME");
    if (tenant == null)
    {
        //
        // The tenant you specified does not exist, or is not enabled.
        return;
    }
    //
    // Get the tenant's pipelines folder
    var pipelinesItem = itemRepo.GetChildren(tenant.ID).FirstOrDefault(c => c[ItemModel.ItemName].Equals("Pipelines"));
    if (pipelinesItem == null)
    {
        //
        // The tenant does not have a pipelines item.
        return;
    }
    //
    // Get the children of the pipelines folder
    var pipelinesItemChildren = itemRepo.GetChildren(pipelinesItem.GetItemId());
    if (!pipelinesItemChildren.Any())
    {
        //
        // The tenant has no pipelines defined.
        return;
    }
    //
    // Create a list to store the pipelines that are found
    var pipelines = new List<Pipeline>();
    foreach(var child in pipelinesItemChildren)
    {
        var converter = child.GetConverter<Pipeline>(itemRepo);
        if (converter == null)
        {
            //
            // The child is not a pipeline, which can happen when
            // pipeline folders are used to organize pipelines.
            //
            // For simplicity, this code does not demonstrate how 
            // to iterate folders.
            continue; 
        }
        var pipeline = converter.Convert(child);
        if (pipeline == null)
        {
            //
            // The item could not be converted into a pipeline.
            continue;
        }
        //
        // It is the responsibility of the client application to respect the
        // setting that indicates whether or not a pipeline is enabled.
        if (pipeline.Enabled)
        {
            pipelines.Add(pipeline);
        }
    }

