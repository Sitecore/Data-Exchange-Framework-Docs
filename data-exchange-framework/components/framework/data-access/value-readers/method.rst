Method
==========================================

This *value reader* is used to invoke a method on a .NET object and return the results.

+-----------------+-----------------------------------------------------------+
| Template name   | **Method Value Reader**                                   |
+-----------------+-----------------------------------------------------------+
| Base template   | :doc:`base-value-reader`                                  |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Method name``                               | The name of the method that is invoked.                   |
+-----------------------------------------------+-----------------------------------------------------------+

Method Parameters
---------------------

Parameters can be passed to the method by adding child items to the 
value reader. The parameters are passed in the order that matches 
the child item positions.  

Parameter items are defined using the following template.  

+-----------------+-----------------------------------------------------------+
| Template name   | **Method Value Reader Parameter**                         |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+-----------------+----------------------------------------------------------------------+
| Field           | Description                                                          |
+=================+======================================================================+
| ``Value``       | The parameter value to be used.                                      |
+-----------------+----------------------------------------------------------------------+
| ``Type``        | Type name for the parameter. For example: ``System.String``          |
+-----------------+----------------------------------------------------------------------+

.. note::

    Method parameters are designed to be static. You must specify the 
    value at design-time (meaning, on the Sitecore definition item).

