Determine if Pipeline Batch Running
=====================================

The *pipeline batch* runs as an asynchronous task on the Sitecore server. This
is done so that you can continue working in Sitecore as the pipeline batch
runs.

But this also means that you will not be notified when the pipeline batch is
finished running. There are, however, a couple of ways you can tell that the
pipeline batch has completed:

Option 1
    The **Run Pipeline Batch** button is disabled while the pipeline batch is
    running. If the button is enabled, you know the pipeline batch is
    completed.

    .. caution::
      This criterion is not 100% reliable. The pipeline batch
      already running is only one reason why the button may be disabled.
      Other reasons include the *tenant* being disabled and no *pipelines*
      being assigned to the pipeline batch.

Option 2
    The **Stop Pipeline Batch** button is enabled while the pipeline batch is
    running. If the button is disabled, you know the pipeline batch is
    running.

Option 3
    The pipeline batch item has a section **Summary**. In this section there 
    is a field **Last Run Finished**. If the value in this field has a 
    date/time value that is equal to or later than the value in the field
    **Requested At**, you know the pipeline batch is completed.

    .. image:: _static/pipeline-batch-summary.png

    |

    .. caution::
      This criteria is not 100% reliable. If an unhandled exception
      is thrown while the pipeline batch is running, the
      pipeline batch will stop running. However, the Last run
      finished value will not be updated.