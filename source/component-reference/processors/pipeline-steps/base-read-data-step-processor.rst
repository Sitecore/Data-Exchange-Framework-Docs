Base Read Data Step Processor
===================================================
This class provides methods to simplify writing pipeline
step processors that read data from an endpoint.

.. |type| replace:: ``Sitecore.DataExchange.Processors.PipelineSteps.BaseReadDataStepProcessor, Sitecore.DataExchange``

+---------------------------+---------------------------------------------------------------------+
| Type                      | |type|                                                              |
+---------------------------+---------------------------------------------------------------------+

ReadData(Endpoint, PipelineStep, PipelineContext, ILogger)
---------------------------------------------------------------------
This method is responsible for reading data from 
the specified endpoint. What the method does with 
the data is up to the developer. Usually the data
is added to a plugin that is added to the 
``PipelineContext``.
