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

.. hint::

    Data Exchange Framework includes a default value mapping. 
    In most cases, this value mapping will be sufficient for 
    any value mapping you configure. It is unlikely that you 
    will need to extend the default value mapping, or to 
    implement your own.
