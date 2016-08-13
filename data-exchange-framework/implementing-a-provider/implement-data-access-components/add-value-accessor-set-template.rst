Add Value Accessor Set Template
=======================================

A *value accessor set* is the component that is used to group a set of
related *value accessor* objects. If a value accessor is like a 
property in c#, a value accessor set is like a class.

There usually is no need to create a custom value accessor set. A value
accessor set can hold any kind of value accessors.

While this is true at the Data Exchange Framework API layer, this is not
usually the case when it comes time to configure a value accessor set.

For example, if you are configuring a value accessor set that represents
the different properties you can read and write on a CRM contact, it is
pretty likely that most - if not all - of your value accessors are of a 
specific type.

So when it comes time to configure a value accessor set, it is often 
helpful to only display value accessors that make sense. This is where 
a custom template can be helpful.

You can create a custom template that only supports certain types of
value accessors. For the file system provider, it makes sense to only
allow value accessors that are based on the **Array Value Accessor**
template. 

This section describes how to create the template that can represent
a value accessor set that is used to define the value accessors that
are used to read values from a text file.   

1. In Sitecore, open Template Manager.
2. Navigate to **Templates > Data Exchange > Providers > File System > Data Access**.
3. Add the following template:

    +-------------------+---------------------------------------------------------------------------------------------+
    | Name              | | **Array Value Accessor Set**                                                              |
    +-------------------+---------------------------------------------------------------------------------------------+
    | Base template     | | **Templates > Data Exchange > Framework > Data Access >**                                 |
    |                   | | **Value Accessors > Value Accessor Set**                                                  |
    +-------------------+---------------------------------------------------------------------------------------------+
    | Location          | | **Templates > Data Exchange > Providers > File System > Data Access**                     |
    +-------------------+---------------------------------------------------------------------------------------------+

4. Set the icon for this template to ``Office/32x32/radio_button_group.png``.
5. Add 