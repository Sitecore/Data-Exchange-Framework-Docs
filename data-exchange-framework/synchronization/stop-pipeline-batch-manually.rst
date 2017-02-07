Stop a Pipeline Batch Manually
=================================

If a *pipeline batch* is currently running...

.. warning::
  Just because you did not start a pipeline batch does not mean it 
  should not be running. There are many reasons why a pipeline batch
  may be running at any given time.

  When a pipeline batch is stopped, any data that was already 
  processed will remain in the system. This can lead to 
  
  Only cancel a pipeline batch if you are certain that you can do 
  so safely.

.. warning::
  When a pipeline batch is stopped, any data that was already 
  processed will remain in the system. This can lead to inconsistent,
  unexpected or corrupted data.
  
  There is no automatic rollback or undo that runs when a pipeline
  batch is stopped. Use this feature with caution.

1.	In Content Editor, navigate to your *tenant*.
2.	Navigate to **Pipeline Batches**.
3.  The child items represent the pipeline batches that are available 
    in your tenant. Select one of the items.
4.	If the pipeline batch is running, the button **Stop Pipeline Batch** will be enabled. Click this button.

    .. image:: _static/stop-pipeline-batch.png

5.	A message will appear that asks you to confirm that you want to indicate the pipeline batch started.

    .. image:: _static/stop-pipeline-batch-confirm.png

    |

    .. note::
        If you click OK, an instruction will be sent to stop the pipeline batch.
        This is handled asynchronously. As a result, the pipeline batch may not 
        stop immediately.
