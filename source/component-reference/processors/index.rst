Processors
===================================================
In Data Exchange Framework, models are used to represent
a part of a sync process that performs a specific purpose.
For example, the model for a pipeline represents the order
of steps that synchronize data (such as sync data from an 
ERP to Sitecore xDB). The model for a pipeline step 
represents a specific function in a pipeline (such as 
read data or map data).

The model represents *what* can be done. The 
implementation of *how* that work is done is 
handled by a processor.

A part of the configuration process is associating a
model with a processor. This is usually pre-configured
in the Sitecore template that represents the model
(using standard values). But it is possible to change
the processor associated with a model at any time.

.. toctree::
   :maxdepth: 1

   pipeline-steps/index.rst