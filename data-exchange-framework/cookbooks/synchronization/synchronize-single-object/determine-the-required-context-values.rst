Determine the Required Context Values
=======================================

After you have determined which *pipeline* needs to run, you must determine
the context values that the steps in the pipeline are expecting.

For pipelines included in Dynamics CRM Connect, this is documented in the 
detailed sequence diagrams available with the product documentation. If 
you are working with a custom pipeline, you will need to determine this 
for yourself.

.. tip:: 
    Detailed sequence diagrams are available for each of the 
    :doc:`/pipeline-batches/index` that are included with Dynamics 
    CRM Connect. A link to the sequence diagram is available on the 
    **overview** page for each pipeline batch. 

The steps in the Pipeline **Upsert Single CRM Contact Pipeline** expect 
the following values be set:

    * Source object is set to the xDB contact
