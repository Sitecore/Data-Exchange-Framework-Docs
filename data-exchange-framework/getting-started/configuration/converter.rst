Converter
=======================================

A *converter* is a component that transforms a Sitecore item model 
into a Data Exchange Framework component. 

There are many converters in Data Exchange Framework. Each component
that is represented by a Sitecore item requires its own converter.

Each Sitecore item that represents a framework component has a field 
``Converter Type`` that is used to identify the converter that is used
to transform the Sitecore item into an instance of the appropriate 
framework component. 

.. hint:: 

    Converters convert objects from one format to another. The format 
    the object from Sitecore is the ``Sitecore.Services.Core.Model.ItemModel.ItemModel``
    type. 

    Using this type makes it possible to read the configuration from
    outside of the Sitecore server, which makes it possible to run
    synchronization processes from outside of the Sitecore server.  