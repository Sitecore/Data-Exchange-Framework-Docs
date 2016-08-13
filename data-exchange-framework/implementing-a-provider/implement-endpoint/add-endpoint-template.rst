Add Endpoint Template
=======================================

An *endpoint* is needed to represent a file that can be read from. 
A template is needed to represent the endpoint. 

1. In Sitecore, open Template Manager.
2. Navigate to **Templates > Data Exchange > Providers > File System**.
3. Add a template folder named **Endpoints**.
4. Add the following template:

    +-------------------+---------------------------------------------------------------------+
    | Name              | **Text File Endpoint**                                              |
    +-------------------+---------------------------------------------------------------------+
    | Base template     | **Templates > Data Exchange > Framework > Endpoints > Endpoint**    |
    +-------------------+---------------------------------------------------------------------+
    | Location          | **Templates > Data Exchange > Providers > File System > Endpoints** |
    +-------------------+---------------------------------------------------------------------+

5. Set the icon for this template to ``Office/32x32/cloud.png``.
6. Add a section named **Settings**.
7. Add the following field:

    +---------+-----------------------------+
    | Name    | **Path**                    |
    +---------+-----------------------------+
    | Type    | **Single-Line Text**        |
    +---------+-----------------------------+
    | Shared  | **ticked**                  |
    +---------+-----------------------------+

8. Add the following field:

    +---------+-----------------------------+
    | Name    | **ColumnSeparator**         |
    +---------+-----------------------------+
    | Type    | **Single-Line Text**        |
    +---------+-----------------------------+
    | Shared  | **ticked**                  |
    +---------+-----------------------------+

9. Navigate to **Templates > Data Exchange > Providers > File System > Endpoints > Text Field Endpoint > Settings > ColumnSeparator**.
10. Set the following field value: 

    +---------+-----------------------------+
    | Name    | **Title**                   |
    +---------+-----------------------------+
    | Value   | **Column separator**        |
    +---------+-----------------------------+

11. Add the following field:

    +---------+---------------------------------------+
    | Name    | **ColumnHeadersInFirstLine**          |
    +---------+---------------------------------------+
    | Type    | **Checkbox**                          |
    +---------+---------------------------------------+
    | Shared  | **ticked**                            |
    +---------+---------------------------------------+

12. Navigate to **Templates > Data Exchange > Providers > File System > Endpoints > Text Field Endpoint > Settings > ColumnHeadersInFirstLine**.
13. Set the following field value: 

    +---------+---------------------------------------+
    | Name    | **Title**                             |
    +---------+---------------------------------------+
    | Value   | **Column headers in first line**      |
    +---------+---------------------------------------+
