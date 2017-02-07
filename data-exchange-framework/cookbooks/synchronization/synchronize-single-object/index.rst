Synchronize Single Object
==========================

A *pipeline batch* is used to run a synchronization task
asynchronously. This is because pipeline batches are designed 
to synchronize multiple records at once. 

However, it is possible to use Dynamics CRM Connect to 
synchronize a specific entity, and to do it synchronously.

This section describes how to trigger the synchronization of 
data from a contact in xDB to a contact in CRM. This could be 
used, for example, to automatically update CRM when a visitor's 
session ends on the website. 

.. note:: 

    While this section covers a specific scenario, the same 
    logic can be used to synchronize any data.

Steps
------

.. toctree::
    :name: synchronize-single-object
    :numbered:
    :titlesonly:

    determine-the-appropriate-pipeline
    determine-the-required-context-values
    run-the-pipeline
