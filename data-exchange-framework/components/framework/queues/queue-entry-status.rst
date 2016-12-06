Queue Entry Status
=============================

The purpose of a work queue is to store data that will be processed 
at some point in the future. There are multiple ways to retrieve 
entries from a queue. One way is based on the status of the entry.

Each entry in a work queue has a status assigned to it. The status
is a flag value, which means that the status value for a specific
entry may be a combination of two or more status codes.

.. note::
    These options are defined in the following location:

    **System > Settings > Data Exchange > Framework > Work Queue Entry Statuses** 

.. note::
    It is up to the queue processor to determine how to use each 
    status code. The descriptions below describe the intended
    purpose of each.

+---------------------------+-----------------------------------------------------------+
| Status                    | Description                                               |
+===========================+===========================================================+
| ``Active``                | The entry is active in the queue.                         |
+---------------------------+-----------------------------------------------------------+
| ``Duplicate``             | A least one other entry represents the same data.         |
+---------------------------+-----------------------------------------------------------+
| ``Entry Does Not Exist``  | The entry does not exist.                                 |
+---------------------------+-----------------------------------------------------------+
| ``Inactive``              | The entry is inactive in the queue.                       |
+---------------------------+-----------------------------------------------------------+
| ``Invalid``               | The entry is invalid.                                     |
+---------------------------+-----------------------------------------------------------+
| ``New``                   | The entry represents                                      |
+---------------------------+-----------------------------------------------------------+
| ``None``                  | No status has been set on the entry.                      |
+---------------------------+-----------------------------------------------------------+
| ``Priority High``         | The entry is a high-priority entry.                       |
+---------------------------+-----------------------------------------------------------+
| ``Priority Low``          | The entry is a low-priority entry.                        |
+---------------------------+-----------------------------------------------------------+
| ``Removed``               | The entry represents data that has been removed.          |
+---------------------------+-----------------------------------------------------------+
| ``Unknown``               | The status of the entry is unknown.                       |
+---------------------------+-----------------------------------------------------------+
| ``Updated``               | The entry represents data that has been updated.          |
+---------------------------+-----------------------------------------------------------+
