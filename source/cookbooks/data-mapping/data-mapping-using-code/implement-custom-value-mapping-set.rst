Implement Custom Value Mapping Set
===================================================
In the data synchronization process, a 
:doc:`/concepts/data-mapping/value-mapping-set` 
controls the mapping of data from the *source object*
to the *target object*. Normally, individual 
:doc:`Value Mappings </concepts/data-mapping/value-mapping>` 
are assigned to the *value mapping set* in order to control 
the data mapping.

In this example, the data mapping will be controlled 
through code. But the *value mapping set* is still
a critical component. It is the component that will
use code to determine the data mapping. So a custom
*value mapping set* is needed.

The following data mapping logic will be implemented:

    * Read the propery ``Name`` from the *source object* and write it to the property ``Description`` on the *target object*.
    * Set the current date on the property ``LastUpdated`` on the *target object*.

1. In Visual Studio, add the following class:

.. code-block:: c#

    using Sitecore.DataExchange.DataAccess;
    using Sitecore.DataExchange.DataAccess.Mappings;
    using Sitecore.DataExchange.DataAccess.Readers;
    using Sitecore.DataExchange.DataAccess.Writers;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;

    namespace Examples.DataExchange
    {
        public class CustomMappingSet : IMappingSet
        {
            public CustomMappingSet() { }

            public ICollection<IMapping> Mappings => throw new NotImplementedException();

            private static IValueReader ValueReader1 = new PropertyValueReader("Name");
            private static IValueWriter ValueWriter1 = new PropertyValueWriter("Description");
            private static IValueWriter ValueWriter2 = new PropertyValueWriter("LastUpdated");
            public bool Run(MappingContext context)
            {
                if (context == null || context.Source == null || context.Target == null)
                {
                    return false;
                }
                ApplyMapping(ValueReader1, ValueWriter1, context, new Mapping { Identifier = "Mapping1" });
                ApplyMapping(DateTime.Now.Date, ValueWriter2, context, new Mapping { Identifier = "Mapping2" });
                return true;
            }
            protected void ApplyMapping(IValueReader reader, IValueWriter writer, MappingContext context, IMapping mapping)
            {
                var context2 = new DataAccessContext();
                var result = reader.Read(context.Source, context2);
                if (!result.WasValueRead)
                {
                    context.RunFail.Add(mapping);
                    return;
                }
                ApplyMapping(result.ReadValue, writer, context, mapping);
            }
            protected void ApplyMapping(object value, IValueWriter writer, MappingContext context, IMapping mapping)
            {
                var context2 = new DataAccessContext();
                var writeSuccess = writer.Write(context.Target, value, context2);
                if (writeSuccess)
                {
                    context.RunSuccess.Add(mapping);
                    return;
                }
                context.RunFail.Add(mapping);
            }
        }
    }
