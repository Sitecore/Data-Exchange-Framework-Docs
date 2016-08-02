Value Mapping Set
=======================================

A *value mapping set* is a collection of *value mapping* objects.

An example of a value mapping set is a collection of value mappings
used to map values from a product from a PIM (product information
system) to a Sitecore item that represents a product. 

A value mapping set also implements the logic to *run* its value 
mappings. When a value mapping set is run, a *mapping context* is 
passed to the value mapping set. This context provides access to
the *source* object and the *target* object.

.. hint::

    Data Exchange Framework includes a default value mapping set. 
    In most cases, this value mapping set will be sufficient for 
    any value mapping set you configure. It is unlikely that you
    will need to extend the default value mapping set, or to 
    implement your own.
