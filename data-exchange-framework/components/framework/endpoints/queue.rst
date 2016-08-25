Queue
==========================================

This template represents a *queue*, which is a data structure that 
can read and write any kind of data.

.. note:: 

    A queue is not limited to a single kind of data. In fact, the kind 
    of data stored in a queue is not usually the defining aspect of a 
    queue. 

    Instead, how or where the queue stores its data usually defines the 
    queue. The default queue that ships with Dynamics CRM Connect is an
    in-memory queue. 

.. tip:: 

    A queue is used to store xDB contact data during the synchronization.
    The benefit of the queue is that it allows the xDB contact to be 
    updated multiple times before the contact is saved to xDB. This
    provides a great improvement in performance. 

+-----------------+-----------------------------------------------------------+
| Template name   | **Endpoint**                                              |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-endpoint`                                      |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Queue type``                                | The .NET type that implements the queue.                  |
+-----------------------------------------------+-----------------------------------------------------------+

