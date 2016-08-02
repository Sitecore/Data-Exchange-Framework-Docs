Process Modeling
=======================================

Data Exchange Framework is used to model and run synchronization
processes. 

Sitecore items are used to model a process. Sitecore templates can
be built to accomodate any kind of data. Content Editor offers a 
rich UI for creating and editing data. And using Sitecore items  
means that Sitecore platform features such as security, versioning, 
workflow and localization are available.

Process modeling is configured using the following components: 

.. toctree::
    :maxdepth: 2
    :titlesonly:

    pipeline
    pipeline-step
    pipeline-processor
    pipeline-step-processor
    pipeline-context
    pipeline-batch
    pipeline-batch-processor

.. note:: 

    If you are familiar with ETL (extract, transform and load) 
    processes, Data Exchange Framework is an ETL layer for Sitecore.
    The parts of a synchronization process map directly to ETL functions.

        * **Extract** - reading data from a *source* system
        * **Transform** - converting the data that was read into a format that is compatible with a *target* system
        * **Load** - writing the data to the target system

