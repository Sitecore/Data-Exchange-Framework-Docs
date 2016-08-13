Add Value Accessor Template
=======================================

A *value accessor* is the component that is used to read a value from 
a *source object* or write a value to a *target object*.

The *pipeline step* read a file and converts each row in the file into 
an array of strings. A value accessor is used to identify the position
in the array you want to use.

Consider an example where you have a file that contains comma-separated 
values (CSV) that provide details about new customers. The file looks
like the following:

    .. code-block:: text
    
        first,last,company
        Aaron,Adkins,Ace Corp
        Brad,Bedford,Burnside Bread
        Charlotte,Colson,Carefree Farms

A template is needed to allow a person configuring a sychronization process
to idenfity that the first name is at position 1, the last name (surname) 
is at position 2 and the company name is at position 3.

1. In Sitecore, open Template Manager.
2. Navigate to **Templates > Data Exchange > Providers > File System**.
3. Add a template folder named **Data Access**.
4. Add the following template:

    +-------------------+---------------------------------------------------------------------------------------------+
    | Name              | | **Array Value Accessor**                                                                  |
    +-------------------+---------------------------------------------------------------------------------------------+
    | Base template     | | **Templates > Data Exchange > Framework > Data Access >**                                 |
    |                   | | **Value Accessors > Value Accessor**                                                      |
    +-------------------+---------------------------------------------------------------------------------------------+
    | Location          | | **Templates > Data Exchange > Providers > File System > Data Access**                     |
    +-------------------+---------------------------------------------------------------------------------------------+

5. Set the icon for this template to ``office/32x32/radio_button_selected.png``.
6. Add a section named **Settings**.
7. Add the following field:

    +---------+-------------------------------------------------------------------------------------------------------+
    | Name    | **Position**                                                                                          |
    +---------+-------------------------------------------------------------------------------------------------------+
    | Type    | **Integer**                                                                                           |
    +---------+-------------------------------------------------------------------------------------------------------+
    | Shared  | **ticked**                                                                                            |
    +---------+-------------------------------------------------------------------------------------------------------+
