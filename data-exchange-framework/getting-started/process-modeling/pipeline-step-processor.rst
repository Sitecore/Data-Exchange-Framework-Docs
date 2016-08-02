Pipeline Step Processor
=======================================

A *pipeline step processor* implements the logic to run a 
*pipeline step*. 

A pipeine step processor is usually tightly coupled with a
pipeline step. The pipeline step represents the configuration
for a part of a pipeline, while the pipeline step processor
implements the logic to use that configuration in order to 
perform a unit of work.

For example, a pipeline step may allow you to specify the CRM
whose contacts you want to read by letting you specify a 
connection string. The pipeline step processor would use the 
connection string to read the contacts from the CRM. 

.. hint:: 

    Data Exchange Framework includes a number of pipeline steps
    and their corresponding pipeline step processors that perform
    basic tasks involved with data exchange, such as the ability 
    to map data from a *source* object and a *target* object. 
    
    However, when building a custom provider for Data Exchange
    Framework, it is very likely you will need to develop custom
    pipeline steps and pipeline step providers. In fact, 
    developing these is one of the main developer tasks involved
    with building a custom provider.
