Pipeline Batch Processor
=======================================

A *pipeline batch processor* implements the logic to run a 
*pipeline batch*. It is responsible for:

    1. Determining the *pipelines* to run
    2. Determining the order in which the pipelines should run
    3. Running the pipelines
    4. Handling errors that occur as the pipelines run  

Each pipeline batch has a pipeline batch processor assigned to it. 
This identifies the pipeline batch processor that is used to run  
the pipeline batch. It also allows each pipeline batch to have its 
own pipeline batch processor assigned.

.. hint:: 

    Data Exchange Framework includes a default pipeline batch processor.
    In most cases, this pipeline batch processor will be sufficient for 
    any pipeline batch you configure. It is unlikely that you will need 
    to extend the default pipeline batch processor, or to implement  
    your own.
