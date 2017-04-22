Resolve Object from Queue
==========================================

This *pipeline step* iterates uses an *endpoint* to search for an 
existing object that matches an identifier value.

+--------------------------------+--------------------------------------------------------------------------+
| Template name                  | **Resolve Object from Queue Pipeline Step**                              |
+--------------------------------+--------------------------------------------------------------------------+
| Base template                  | :doc:`base-resolve-object`                                               | 
+--------------------------------+--------------------------------------------------------------------------+

+-------------------------------------+---------------------------------------------------------------------+
| Field                               | Description                                                         |
+=====================================+=====================================================================+
| ``Endpoint From``                   | | The *work queue* endpoint used to search for the identifier value.|
+-------------------------------------+---------------------------------------------------------------------+
| ``Default Work Queue Entry Status`` | | Status for the work queue entry if the status is not already      |
|                                     | | set (such as for new entries).                                    |
|                                     | |                                                                   |
|                                     | | Additional logic is used if the work queue entry represents an    |
|                                     | | object from a repository. If the status from the repository is    |
|                                     | | unknown, this is the status that is set on the entry.             |
+-------------------------------------+---------------------------------------------------------------------+
