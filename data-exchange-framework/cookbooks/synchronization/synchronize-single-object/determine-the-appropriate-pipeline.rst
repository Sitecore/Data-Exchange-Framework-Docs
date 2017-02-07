Determine the Appropriate Pipeline
===================================

Running a synchronization process normally involves running a 
*pipeline batch*. But pipeline batches are designed to handle 
sets of data, and to be run asynchronously.

In this case, the synchronization only handles a single object, 
and it needs to run synchronously. Specifically, it needs to 
handle a single xDB contact. 

The pipeline batch **xDB Contacts to CRM Sync Pipeline Batch** 
contains this logic. By looking at the *pipelines* that this 
pipeline batch runs, you can see that the pipeline 
**Upsert Single CRM Contact Pipeline** is responsible for 
handling a single xDB contact. This is the pipeline you are 
looking for.

Note the item ID for the pipeline definition item.
