Add Pipline Step to Resolve Target Item
===========================================================

The first *pipeline step* determines whether or not a Sitecore item 
already exists for the row from the text file.

1. Navigate to the *pipeline* **City Info from File to City Info Item Sync Pipeline**.
2. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Resolve Sitecore Item Pipeline Step**                             |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **Resolve City Info Item**                                          |
    +-------------------+---------------------------------------------------------------------+

3. Set the following field values:

    +-------------------------------------------+-----------------------------------------------------------+
    | Field                                     | Value                                                     |
    +===========================================+===========================================================+
    | Template for New Item                     | | **Templates > User Defined >**                          |
    |                                           | | **City Information**                                    |
    +-------------------------------------------+-----------------------------------------------------------+
    | Item Name Value Accessor                  | | **Data Access > Value Accessor Sets >**                 |
    |                                           | | **Providers > File System >**                           |
    |                                           | | **File System > City Information File**                 |
    |                                           | | **Fields > City**                                       |
    +-------------------------------------------+-----------------------------------------------------------+
    | Endpoint From                             | | **Sitecore > Sitecore Database Endpoint**               |
    +-------------------------------------------+-----------------------------------------------------------+
    | Identifier Value Accessor                 | | **Value Accessor Sets > Providers >**                   |
    |                                           | | **File System > City Information File Fields >**        |
    |                                           | | **Identifier**                                          |
    +-------------------------------------------+-----------------------------------------------------------+
    | Identifier Object Location                | | **Pipeline Context Source**                             |
    +-------------------------------------------+-----------------------------------------------------------+
    | Resolved Object Location                  | | **Pipeline Context Target**                             |
    +-------------------------------------------+-----------------------------------------------------------+
    | Parent for Item                           | | **sitecore > content > Cities**                         |
    +-------------------------------------------+-----------------------------------------------------------+
    | Matching Field Value Accessor             | | **Data Access > Value Accessor Sets >**                 |
    |                                           | | **Providers > Sitecore > City Information**             |
    |                                           | | **Item Fields > Identifier**                            |                         
    +-------------------------------------------+-----------------------------------------------------------+

    .. hint:: 
    
        Hopefully, most of the fields are self-explanatory. One field 
        that may be confusing to you is **Identifier Object Location**.
        The *pipeline step processor* uses this field to determine where
        to find the source object.

        This value is specified in the pipeline step processor that 
        iterates the data that is read from the text file. This is 
        configured in a later step. 

4. Save the item.

The pipeline in Content Editor.

.. image:: _static/resolve-target-pipeline-step-created.png
