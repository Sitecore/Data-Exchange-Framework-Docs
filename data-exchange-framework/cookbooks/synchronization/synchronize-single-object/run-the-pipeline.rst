Run the Pipeline
=======================================

The following code demonstrates how to run the *pipeline* 
**Upsert Single CRM Contact Pipeline**.

.. note:: 

    The code assumes you have already resolved the xDB contact you want 
    to use to update CRM. This contact is accessed through the variable 
    contact.

.. note::

    The code uses extension methods defined in the namespace 
    ``Sitecore.DataExchange.Extensions``, so you must import 
    this namespace in your code.

.. code-block:: c#

    Contact contact = ... //contact comes from the tracker or from somewhere else
    Guid pipelineItemId = Guid.Parse("####"); //item id for the pipeline definition item
    IItemModelRepository itemModelRepo = Sitecore.DataExchange.Context.ItemModelRepository;
    ItemModel model = itemModelRepo.Get(pipelineItemId);
    IConverter<ItemModel, Pipeline> converter = model.GetConverter<Pipeline>(itemModelRepo);
    Pipeline pipeline = converter.Convert(model);
    IPipelineProcessor processor = pipeline.PipelineProcessor;
    PipelineBatchContext batchContext = new PipelineBatchContext();
    PipelineContext pipelineContext = new PipelineContext(batchContext);
    pipelineContext.Plugins.Add(new SynchronizationSettings { Source = contact });
    if (processor.CanProcess(pipeline, pipelineContext))
    {
      processor.Process(pipeline, pipelineContext);
      if (!pipelineContext.CriticalError)
      {
        //success
      }
    }

