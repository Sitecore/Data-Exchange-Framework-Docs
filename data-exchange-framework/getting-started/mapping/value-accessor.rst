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

.. note::

    Data Exchange Framework includes a number of value accessors.
    More information on those components is available in the
    :doc:`../../components/index` section, under 
    :doc:`../../components/framework/data-access/value-accessors/index`.

.. hint::

    Custom value accessor templates make it easier to configure
    a tenant. Consider the requirement to support reading and  
    writing properties on CRM entities. 
    
    The act of reading and writing different properties only 
    differs by the name of the property being accessed. A
    custom value accessor template lets users specify the 
    property name once. The value accessor itself is able
    to create the appropriate value reader and value writer
    for the specific property.

    The need for the value reader and value writer still exists, 
    but the need to configure each separately does not.
