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

.. note::

    Data Exchange Framework includes a default value mapping set.
    More information on this component is available in the
    :doc:`../../components/index` section, under 
    :doc:`../../components/framework/data-mapping/value-mappings/value-mapping-set`.

.. hint::

    If you are developing a custom provider, it is likely you will 
    develop custom value mapping sets. 
