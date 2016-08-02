Iterating Data
=======================================

Often, the data that is read from an endpoint represents a collection 
of objects, where each object must be processed individually. 

For example, consider a case where products are read from a PIM 
(product information system). A *pipeline* is designed
to handle each product. So the data that is read must be iterated,
and each product must be passed individually to the pipeline.

Data Exchange Framework includes the components that are needed to
support this scenario. The developer building the pipelines step
processor that reads the products from the PIM must set the 
products in the *pipeline context* using the 
``Sitecore.DataExchange.Plugins.IterableDataSettings`` plugin. 

The next pipeline step in the pipeline is a step is the 
``Iterate Data and Run Pipelines Pipeline Step`` pipeline step.
This step finds the ``IterableDataSettings`` plugin and iterates 
the data in the collection set on the plugin (in this case, the 
products that were set by the previous pipeline step processor). 

The pipeline step has a property ``Pipelines`` property. This 
property identifies the pipelines that are run for each object 
in the collection.