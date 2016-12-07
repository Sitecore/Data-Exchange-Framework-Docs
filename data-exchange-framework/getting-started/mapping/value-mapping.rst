Value Mapping
=======================================

A *value mapping* is a component that associates the  
*value accessor* used to read a value from a *source*
object with the *value accessor* used to write a value
to a *target object*. 

An example of a value mapping is one that specifies how to
read the description of a product from a PIM (product 
information system) and write that description to a field 
on a Sitecore item that represents the product.  

.. note::

    Data Exchange Framework includes a default value mapping.
    More information on this component is available in the
    :doc:`../../components/index` section, under 
    :doc:`../../components/framework/data-mapping/value-mappings/value-mapping`.

.. hint::

    If you are developing a custom provider, it is likely you will 
    develop custom value mappings. 
