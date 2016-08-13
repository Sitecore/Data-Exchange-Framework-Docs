Set Standard Values on Value Accessor Set Template
===========================================================

1. In Sitecore, open Template Manager.
2. Navigate to **Templates > Data Exchange > Providers > File System > Data Access > Array Value Accessor Set**.
3. Add the Standard Values item.
4. Navigate to the Standard Values item.
5. Set the following field value:

    +---------+---------------------------------------------------------------------------------------------------------------------------+
    | Name    | **Converter type**                                                                                                        |
    +---------+---------------------------------------------------------------------------------------------------------------------------+
    | Value   | **Sitecore.DataExchange.Converters.DataAccess.ValueAccessors.ChildBasedValueAccessorSetConverter, Sitecore.DataExchange** |
    +---------+---------------------------------------------------------------------------------------------------------------------------+

    .. note:: 
    
        Data Exchange Framework provides a converter that is able to 
        read the child items from the item is it converting, and use
        the converter on the child item to convert the child item.

        Since this template is only needed to simplify configuration,
        there is no need to add any functionality. This means you can
        use the converter that is already available.

6. In the Insert Options, assign the template **Templates > Data Exchange > Providers > File System > Data Access > Array Value Accessor**.
