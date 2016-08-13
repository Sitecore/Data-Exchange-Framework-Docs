Implement Value Accessor Converter
=======================================

A *converter* is needed to convert a Sitecore item that represents 
a *value accessor* into a value accessor component for Data Exchange 
Framework.

1. In Visual Studio, add the following class:

    .. code-block:: c#
    
        using Sitecore.Services.Core.Model;
        using System;

        namespace Examples.FileSystem.Models.ItemModels.DataAccess
        {
            public class ArrayValueAccessorItemModel : ItemModel
            {
                public const string Position = "Position";
            }
        }
    
    .. note:: 
    
        This class defines constants for the names of the fields from 
        the value accessor template. These field names are referenced  
        by the converter.
        
        In order for the converter to be able to run inside or outside
        of the Sitecore server, the type ``Sitecore.Services.Core.Model.ItemModel``
        is used to represent Sitecore items. Fields on this type are 
        accessed by name.
        
        This stands in contrast to how field are accessed on ``Sitecore.Data.Items.Item``.
        In this type, fields can be accessed by name or ID, with ID 
        being the preferred value since it is unlikely to change.

2. Add the following class:

    .. code-block:: c#

        using Examples.FileSystem.Models.ItemModels.DataAccess;
        using Sitecore.DataExchange.Converters.DataAccess.ValueAccessors;
        using Sitecore.DataExchange.DataAccess;
        using Sitecore.DataExchange.DataAccess.Readers;
        using Sitecore.DataExchange.DataAccess.Writers;
        using Sitecore.DataExchange.Repositories;
        using Sitecore.Services.Core.Model;
        using System;

        namespace Examples.FileSystem.Converters.DataAccess.ValueAccessors
        {
            public class ArrayValueAccessorConverter : ValueAccessorConverter
            {
                private static readonly Guid TemplateId = Guid.Parse("[VALUE ACCESSOR TEMPLATE ID]");
                public ArrayValueAccessorConverter(IItemModelRepository repository) : base(repository)
                {
                    this.SupportedTemplateIds.Add(TemplateId);
                }
                public override IValueAccessor Convert(ItemModel source)
                {
                    var accessor = base.Convert(source);
                    if (accessor == null)
                    {
                        return null;
                    }
                    var position = base.GetIntValue(source, ArrayValueAccessorItemModel.Position);
                    if (position <= 0)
                    {
                        return null;
                    }
                    //
                    //array position is 1-based in the Sitecore item but is 0-based in the reader/writer
                    position--;
                    //
                    //unless a reader or writer is explicitly set use the property value
                    if (accessor.ValueReader == null)
                    {
                        accessor.ValueReader = new ArrayValueReader(position);
                    }
                    if (accessor.ValueWriter == null)
                    {
                        accessor.ValueWriter = new ArrayValueWriter(position);
                    }
                    return accessor;
                }

            }
        }

    .. important:: 

        You must change the value of ``[VALUE ACCESSOR TEMPLATE ID]`` 
        to match the id from the value accessor template you created.
        
    .. hint:: 
    
        By inheriting from ``BaseEndpointConverter<ItemModel>`` you  
        get access to a number of methods that facilitate reading 
        values from fields on a Sitecore item. 

        In addition to being able to read simple values like strings,
        numbers and dates, methods are available to automatically 
        convert referenced items into the appropriate Data Exchange
        Framework component.

        See the API documentation for more information.
