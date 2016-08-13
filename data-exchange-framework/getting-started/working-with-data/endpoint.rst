Endpoint
=======================================

An *endpoint* represents a data source. The data source may support 
the ability to read data, to write data, or to both read and write 
data.

Examples of endpoints are:

    * URL for a web service used to read data from a CRM
    * Path to a directory used to read files
    * Connection string used to connect to a relational database

.. note:: 

    The endpoint does not provide the ability to interact with  
    the data source. It simply represents the data source. 
    
    Data Exchange Framework uses separate components to represent 
    the data source (endpoint) and the logic used to interact 
    with the data source (*pipeline step processor*).