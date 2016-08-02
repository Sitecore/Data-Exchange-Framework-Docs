Pipeline Processor
=======================================

A *pipeline processor* implements the logic to run a *pipeline*.
It is responsible for:

    1. Determining the *pipeline steps* to run
    2. Determining the order in which the pipeline steps should run
    3. Running the pipeline steps
    4. Handling errors that occur as the pipeline steps run  

Each pipeline has a pipeline processor assigned to it. This 
identifies the pipeline processor that is used to run the 
pipeline. It also allows each pipeline to have its own
pipeline processor assigned.

.. hint:: 

    Data Exchange Framework includes a default pipeline processor.
    In most cases, this pipeline processor will be sufficient for 
    any pipeline you configure. It is unlikely that you will need 
    to extend the default pipeline processor, or to implement  
    your own.
