Read Sitecore Items
=============================

This *pipeline step* is used to read items from a Sitecore database.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Read Sitecore Items Pipeline Step**                                 |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Endpoint From``                 | | The Sitecore `endpoint <../endpoints/>`_ used to read items from.   |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Item Root``                     | | The item to use as the starting point for the search. In other      |
|                                   | | words, limit the search to the selected item and its descendants.   |
|                                   | |                                                                     |
|                                   | | This value is not required.                                         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Templates``                     | | The search is limited to items based on the selected templates.     |
|                                   | |                                                                     |
|                                   | | This value is not required.                                         |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Page Size``                     | | It is possible that a large number of items will match the          | 
|                                   | | specified search criteria. In order to avoid performance problems   |
|                                   | | that occur when large amounts of data are loaded at once, a         |
|                                   | | maximum number of items are read at one time. This setting          |
|                                   | | specifies that maximum number.                                      |
|                                   | |                                                                     |
|                                   | | Note: This value does not limit the number of items that are read.  |
|                                   | | For example, if 100 items are found but the value is 20, 5          |
|                                   | | separate calls will be made to the Sitecore server in order to read |
|                                   | | all 100 items.                                                      | 
|                                   | |                                                                     |
|                                   | | If no value is specified, the underlying component that is          |
|                                   | | responsible for performing the search determines the value to use.  |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Max Count``                     | | The maximum number of items that will be handled, even if the       |
|                                   | | returns more items.                                                 |                    
|                                   | |                                                                     |
|                                   | | For example, if the search returns 100 items but this value is set  |
|                                   | | to 20, only the first 20 items will be available to subsequent      |
|                                   | | steps.                                                              |
|                                   | |                                                                     |
|                                   | | The value 0 means that there is no limit to the number of items     |
|                                   | | that are handled. In other words, all of the items that are         | 
|                                   | | returned by the search will be handled.                             |
+-----------------------------------+-----------------------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``IterableDataSettings``          | | Subsequent pipeline steps use this plugin to access the items       |
|                                   | | read from a Sitecore database.                                      |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
