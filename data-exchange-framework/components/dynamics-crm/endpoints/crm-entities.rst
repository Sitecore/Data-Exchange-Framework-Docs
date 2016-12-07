Entities
==========================================

This template represents the ability to interact with an *entity repository set*.
An entity repository set provides the ability to interact with CRM entities.

+-----------------+-----------------------------------------------------------+
| Template name   | **Dynamics CRM Entity Endpoint**                          |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`../../framework/endpoints/base-endpoint`            |
+-----------------+-----------------------------------------------------------+

+--------------------------+--------------------------------------------------------------------------------+
| Field                    | Description                                                                    |
+==========================+================================================================================+
| ``Entity Repository Set``| | The entity repository set that is available from the endpoint.               |
+--------------------------+--------------------------------------------------------------------------------+
| ``Max Retries``          | | When a component interacts with the entity repository set, a failure         |
|                          | | may occur. This value tells the component to retry up to a certain           |
|                          | | number of times before returning an error.                                   |
+--------------------------+--------------------------------------------------------------------------------+
| ``Retry Interval``       | | This value tells the component that is able retry an operation to wait       |
|                          | | a certain amount of time before retrying the operation.                      |
+--------------------------+--------------------------------------------------------------------------------+
