Pipeline Context
=======================================

The *pipeline context* is used to pass information between the
different *pipeline step processors* that are run when a pipeline 
is run. 

When a pipeline is started, a pipeline context is created. When 
a pipeline step processor is run, this context is passed to the 
processor. The same pipeline context is passed to each processor.
This provides a way for data to be passed from one processor to
another.

.. hint:: 

    If you are familiar with Sitecore pipelines, a pipeline context
    serves the same purpose as the ``Sitecore.Pipelines.PipelineArgs``
    type.
    