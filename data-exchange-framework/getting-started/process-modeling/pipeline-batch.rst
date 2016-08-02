Pipeline Batch
=======================================

A *pipeline batch* provides the ability to run one or more *pipelines*.

In one way, a pipeline batch is similar to a *pipeline*. A pipeline 
is a collection of *pipeline steps* that are run in a specific
order. A pipeline batch is a collection of pipelines that are
run in a specific order.

But there is more to a pipeline batch than just the pipelines that
are assigned to the batch. A pipeline batch also:

    * Keeps track of when it was last run
    * Maintains a log of activity from when it was last run
    * Can be started directly from the Sitecore Content Editor
    * Can be scheduled using Sitecore Tasks 
