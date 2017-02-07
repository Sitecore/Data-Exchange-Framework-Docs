Data Exchange Framework
=================================================

.. contents:: What's new in version 1.3
   :depth: 2
   :local:

New features
-----------------------------

Improved control over work queue processing
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A *work queue processor* only processes entries whose status matches 
one of the specified status values. 

A setting allows you to configure whether or not unprocessed 
queue entries are automatically removed from the queue after 
the processor runs.

For more information, see :doc:`../../components/framework/queues/queue-processors/base-queue-processor`.

Improved feedback when stopping pipeline batch that is running
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When a user manually stops a *pipeline batch*, a message is displayed to 
the user that confirms the pipeline batch is being stopped.

Improved Item Model Repository functionality
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A delete method has been added to ``IItemModelRepository``.

Action for insert option rules that adds children as insert options
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The action is defined in the Sitecore database under 
**/sitecore/system/Settings/Rules/Definitions/Elements/Insert Options/Data Exchange - Add Children as Insert Options**.

Templates were organized into folder and existing insert option rules were changed to use this new action.

API changes
-----------------------------

    * Added base type ``BaseWorkQueueProcessor`` for *work queue processors*.
    * Marked interface ``IDataChanged`` obsolete.
    * Added support for language and versions on ``IItemModelRepository``.
    * Overloaded method for creating new items on ``IItemModelRepository``.
    * Added virtual method on ``InProcItemModelRepository`` that determines whether or not Sitecore is running in the cloud.
    * Renamed namespace ``Sitecore.DataExchange.ApplyMappingActions`` to ``Sitecore.DataExchange.MappingsAppliedActions``.
    * Renamed namespace ``Sitecore.DataExchange.DataAccess.ApplyMappingActions`` to ``Sitecore.DataExchange.DataAccess.MappingsAppliedActions``.
    * Added async support on ``ITenantRepository``.

Bugs fixes
-----------------------------

    * Pipeline batch summary values are not set when using the remote API to run the pipeline batch (122300)
    * Incorrect encoding used in ``WebApiItemModelRepository`` (142680)
