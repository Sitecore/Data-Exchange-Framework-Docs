Pipeline Steps
=======================================

A *pipeline step* represents a unit of work that is performed when 
a *pipeline* runs. Configuring pipeline steps, and ensuring those
steps are in the correct order, is one of the most important parts
of configuring a synchronization process.

At runtime, parameters are made available to a pipeline step through
*pipeline context plugins*. Knowing which plugins provide input to
a pipeline step - and which plugins are provide output from a 
pipeline step - is critical in order to be able to use a pipeline 
step.  

.. note::
    These templates are defined in the following location:

    **Templates > Data Exchange > Framework > Pipeline Steps** 

.. toctree::
    :name: framework-pipeline-steps-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    apply-mapping
    iterate-data-and-run-pipelines

.. toctree::
    :name: framework-pipeline-steps-base-templates
    :caption: Base Templates 
    :titlesonly:
    :maxdepth: 2

    base-pipeline-step
    base-process-queue
    base-process-queue-from-endpoint
    base-resolve-object
    base-resolve-object-from-queue
