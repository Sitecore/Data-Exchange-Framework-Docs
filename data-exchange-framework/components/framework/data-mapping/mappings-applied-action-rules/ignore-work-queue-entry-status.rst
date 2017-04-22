Ignore Work Queue Entry Status
==========================================

.. |status| replace:: :doc:`/components/framework/queues/queue-entry-status`

This *mappings applied action rule* is used to prevent a *mappings applied action*
from running if the |status| of the *work queue entry* associated with the action
is a certain value.

.. important::

    This rule can only be assigned to actions that inherit from 
    ``Sitecore.DataExchange.DataAccess.MappingsAppliedActions.IUpdateWorkQueueStatusAction``.
    This interface specifies a method that is used to resolve the *work queue entry*
    that is associated with the action.

+-----------------+-----------------------------------------------------------+
| Template name   | **Update Work Queue Entry Status Action**                 |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-mappings-applied-action-rule`                  |
+-----------------+-----------------------------------------------------------+

+-------------------------------------+-----------------------------------------------------------+
| Field                               | Description                                               |
+=====================================+===========================================================+
| ``Ignore Entries``                  | | If the |status| is one of the values selected in this   |
|                                     | | field, the rule returns false, which will prevent the   |
|                                     | | *mappings applied action* from running.                 |
+-------------------------------------+-----------------------------------------------------------+
