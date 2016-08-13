Item Model Repository
=======================================

An *item model repository* is a component used to read items from a 
Sitecore database. 

A *converter* is responsible for transforming a Sitecore item into
a Data Exchange Framework component. There are cases when the Sitecore
item has fields that reference other Sitecore items. In order to handle
these fields, the converter must be able to follow the references.
The item model repository is used to do this. 
 
.. hint:: 

    A converter may run inside or outside of the Sitecore server.
    Therefore, it is important that the method for following 
    references uses an API that is only available in both cases. 
    
    Item model repository is a layer of abstraction that can be 
    used in both cases.
