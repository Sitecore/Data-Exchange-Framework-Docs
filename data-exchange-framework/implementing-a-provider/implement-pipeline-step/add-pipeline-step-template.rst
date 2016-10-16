Add Pipeline Step Template
=======================================

A *pipeline step* is needed to represent a logic involved with 
reading a file from an endpoint and handling the data that is read.

A template is needed to represent the pipeline step. It allows the
pipeline step to be configured. 

1. In Sitecore, open Template Manager.
2. Navigate to **Templates > Data Exchange > Providers > File System**.
3. Add a template folder named **Pipeline Steps**.
4. Add the following template:

    +-------------------+-----------------------------------------------------------------------------------+
    | Name              | **Read Text File Pipeline Step**                                                  |
    +-------------------+-----------------------------------------------------------------------------------+
    | Base template     | **Templates > Data Exchange > Framework > Pipeline Steps > Pipeline Step**        |
    +-------------------+-----------------------------------------------------------------------------------+
    | Location          | **Templates > Data Exchange > Providers > File System > Pipeline Steps**          |
    +-------------------+-----------------------------------------------------------------------------------+

5. Set the icon for this template to ``office/32x32/element.png``.
6. Add a section named **Endpoints**.
7. Add the following field:

    +---------+-----------------------------------------------------------------------------------------------------------------------------------------------+
    | Name    | **EndpointFrom**                                                                                                                              |
    +---------+-----------------------------------------------------------------------------------------------------------------------------------------------+
    | Type    | **Droptree**                                                                                                                                  |
    +---------+-----------------------------------------------------------------------------------------------------------------------------------------------+
    | Source  | ``query:./ancestor-or-self::*[@@templateid='{327A381B-59F8-4E88-B331-BEBC7BD87E4E}']//descendant-or-self::*[@@templateid='TEMPLATE-ID']``     |
    +---------+-----------------------------------------------------------------------------------------------------------------------------------------------+
    | Shared  | **ticked**                                                                                                                                    |
    +---------+-----------------------------------------------------------------------------------------------------------------------------------------------+

    .. important:: 
    
        You must replace ``TEMPLATE-ID`` with the id for the template
        you created named **File System Endpoints Root**. This is the  
        template that represents folder used to store endpoint items
        for your provider. 

    .. note:: 
    
        The query used for this field limits the droptree to the endpoints 
        in the current tenant that are in the folder used to organize 
        endpoints for this provider. 
        
        The id **{327A381B-59F8-4E88-B331-BEBC7BD87E4E}** is for the template
        that represents a tenant. This is a template that is provided with the
        framework. You should not change this value. 
        
        The id you provide is for the item used organize the endpoints for 
        this provider. 
        
8. Navigate to **Templates > Data Exchange > Providers > File System > Pipeline Steps > Read Text File Pipeline Step > Endpoints > EndpointFrom**.
9. Set the following field value: 

    +---------+---------------------------------------+
    | Name    | **Title**                             |
    +---------+---------------------------------------+
    | Value   | **Endpoint for the file to read**     |
    +---------+---------------------------------------+
