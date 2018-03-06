Implement Value Accessor Converter
===================================================
In this example, a converter is needed to convert the 
settings on a value accessor item into a plugin that
identifies the endpoint that the pipeline step will
read from.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.Attributes;
    using Sitecore.DataExchange.Converters.DataAccess.ValueAccessors;
    using Sitecore.DataExchange.DataAccess;
    using Sitecore.DataExchange.DataAccess.Readers;
    using Sitecore.DataExchange.DataAccess.Writers;
    using Sitecore.DataExchange.Repositories;
    using Sitecore.Services.Core.Model;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DataExchange.Providers.FileSystem
    {
        [SupportedIds(ArrayValueAccessorTemplateId)]
        public class ArrayValueAccessorConverter : ValueAccessorConverter
        {
            public const string ArrayValueAccessorTemplateId = "[ARRAY VALUE ACCESSOR TEMPLATE ID]";
            public const string TemplateFieldPosition = "Position";
            public ArrayValueAccessorConverter(IItemModelRepository repository) : base(repository)
            {
            }
            protected override IValueReader GetValueReader(ItemModel source)
            {
                var reader = base.GetValueReader(source);
                if (reader == null)
                {
                    var position = this.GetIntValue(source, TemplateFieldPosition);
                    if (position < 0)
                    {
                        return null;
                    }
                    reader = new ArrayValueReader(position);
                }
                return reader;
            }
            protected override IValueWriter GetValueWriter(ItemModel source)
            {
                var writer = base.GetValueWriter(source);
                if (writer == null)
                {
                    var position = this.GetIntValue(source, TemplateFieldPosition);
                    if (position < 0)
                    {
                        return null;
                    }
                    writer = new ArrayValueWriter(position);
                }
                return writer;
            }
        }
    }

.. important::

    You must change the value of ``[ARRAY VALUE ACCESSOR TEMPLATE ID]``
    to match the id from the value accessor template named **Array Value Accessor**.

2. Compile the project.
3. Deploy **Examples.DataExchange.Providers.FileSystem.dll** to the Sitecore server.