Value Accessor
=======================================

A *value accessor* is a component that associates a 
*value reader* with a *value writer*. 

An example of a value accessor is a value accessor used to
read or write the a field on a Sitecore item that represents
a product.

.. hint:: 

    A value accessor is like a .NET property. A value reader is
    like a property getter. A value writer is like a property
    setter. 

.. hint::

    Data Exchange Framework includes a default value accessor. 
    In most cases, this value accessor will be sufficient for 
    any value accessor you configure. It is unlikely that you 
    will need to extend the default value accessor, or to 
    implement your own.
