Base Pipeline Step Converter
===================================================
This class provides methods to simplify reading values
from Sitecore items that are set on plugins that are
added to a pipeline step for Data Exchange Framework.

.. |type| replace:: ``Sitecore.DataExchange.Converters.PipelineSteps.BasePipelineStepConverter, Sitecore.DataExchange``

+---------------------------+---------------------------------------------------------------------+
| Type                      | |type|                                                              |
+---------------------------+---------------------------------------------------------------------+

AddPlugins(ItemModel, PipelineStep)
---------------------------------------------------
This method is used to add plugins to the pipeline step.

AddRequiredPlugins(ItemModel, PipelineStep)
---------------------------------------------------
The processor that implements the logic for a pipeline step
may expect certain plugins be added to the pipeline in order
for the processor to run properly. For example, a processor 
that reads data from an endpoint requires a plugin that 
specifies the endpoint.

This method is used to add the plugins to the pipeline step 
that the processor requires. This method does not do anything 
special when it adds the plugins. The method is separate from
``AddPlugins(ItemModel, PipelineStep)`` to help the code 
self-document.

AddOverrideActionsPlugin(ItemModel, PipelineStep)
---------------------------------------------------
There are cases where the pipeline step processor must be
determined at runtime. Override actions are used to define
the rules that determine which processor to use.

.. note::

    It is unusual for a developer to override this method.