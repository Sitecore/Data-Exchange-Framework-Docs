Reading Data
=======================================

Providing the ability to read data in a synchronization process  
requires a *pipeline step* be implemented. When the pipeline 
step is configured, an *endpoint* is selected. 

The *pipeline step processor* implements the following logic:  

    * Reads data from the endpoint
    * Does something with the data that was read (such as putting  
      the data into the *pipeline context* so that a subsequent  
      pipeline step processor can handle the data)
