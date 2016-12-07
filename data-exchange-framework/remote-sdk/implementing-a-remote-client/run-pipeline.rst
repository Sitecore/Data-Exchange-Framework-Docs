Run Pipeline
=======================================


.. important:: 

    Unlike a pipeline batch, a pipeline does not indicate whether
    or not it can safely be called using the remote API. Therefore
    it is the responsibility of the developer to understand the 
    pipelines before attempting to use them. 

.. important:: 

    When it comes time to run a *pipeline*, providing an example 
    is challenging. This is not because it is difficult to run a  
    pipeline batch. This is handled in a few line of code. 

    The challenging part is that before you can run a pipeline, 
    you must create a *pipeline context*, and you must set 
    values on the context that are used by the *pipeline steps* 
    that make up the pipeline. It is impossible to predict what 
    those values must be.

    In order to run a pipeline using the remote API, you must 
    understand the context requirements of the pipeline you 
    want to run.

.. important:: 

    This code assumes the following namespaces are included by the ``using`` directive:

        * Sitecore.DataExchange.Contexts
        * Sitecore.DataExchange.Models
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
	// Get your tenant.
	var tenant = repo.GetTenants().FirstOrDefault(t => t.Enabled && t.Name == "YOUR TENANT NAME");
	if (tenant == null)
	{
		//
		// The tenant you specified does not exist, or is not enabled.
		return;
	}
	//
	// Get the pipeline from the tenant.
	var pipeline = repo.GetPipelines(tenant.ID, true)
                           .FirstOrDefault(p => p.Enabled && p.Name == "YOUR PIPELINE NAME");
	if (pipeline == null)
	{
	    return;
	}
	//
	// Get the pipeline's processor, which is the component that
	// implements the logic needed to run the pipeline.
	var processor = pipeline.PipelineProcessor;
	if (processor == null)
	{
	    return;
	}
	//
	// Create the context used to pass data to the pipeline,
	// and for steps in the pipeline to read and write data.
	//
	// Depending on the pipeline, you may need to add plugins
	// to the pipeline context in order to provide input to
	// the pipeline. Consult the documentation for the
	// specific pipeline for more information.
	var pipelineContext = new PipelineContext(new PipelineBatchContext());
	if (!processor.CanProcess(pipeline, pipelineContext))
	{
	    return;
	}
	//
	// Run the pipeline's processor, which is how a pipeline is run.
	processor.Process(pipeline, pipelineContext);
	if (pipelineContext.CriticalError)
	{
	    return;
	}
