Start a Pipeline Batch Programmatically
========================================

*Pipeline batches* can be started programmatically using the following code:

.. code-block:: c#

  Guid tenantId = ...         //tenant that owns the pipeline batch
  Guid pipelineBatchId = ...  //pipeline batch
  IEnumerable<PipelineBatch> batches = null;
  batches = Sitecore.DataExchange.Context.TenantRepository.GetPipelineBatches(tenantId);
  if (batches != null)
  {
    PipelineBatch pipelineBatch = batches.FirstOrDefault(x => x.ID == pipelineBatchId);
    if (pipelineBatch != null)
    {
      var runner = new InProcessPipelineBatchRunner();
      if (runner.Run(pipelineBatch))
      {
        //pipeline batch was started
      }
    }
  }

.. tip::
  Depending on the pipeline batch you run, it may take a long time
  for the batch to complete. Unless you are certain that the pipeline
  batch will finish is a short amount of time, you may prefer to run
  the pipeline batch in a Sitecore *task*.
