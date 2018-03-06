Implementing a Troubleshooter
===================================================
A troubleshooter is a component that lets a Sitecore 
user run logic that determines whether the selected
Sitecore item is configured or working properly.

This example adds functionality to the file system
provider configured in :doc:`../implementing-a-provider/index`.
It adds a troubleshooter that can determine whether
a file system endpoint is configured to use a file
that the Sitecore server has access to.

.. hint::

    Troubleshooters were originally designed for endpoints.
    They are used to let a user determine whether an endpoint
    is configured properly. This remains the primary use of
    troubleshooters, but they can be used on any type of item,
    provided the item inherits from the following Data Exchange
    Framework base templates:

        * **Convertible**
        * **Troubleshootable**

.. note::

    Finished code and installation packages are available in 
    `GitHub <https://github.com/Sitecore/Sitecore.DataExchange.Examples/>`_. 

.. toctree::
   :maxdepth: 1

   implement-component.rst
   specify-troubleshooter-on-endpoint.rst
   test-troubleshooter.rst