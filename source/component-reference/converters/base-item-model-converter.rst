Base Item Model Converter
===================================================
This class provides methods to simplify reading values
from Sitecore items that are set on Data Exchange
Framework model objects.

.. |type| replace:: ``Sitecore.DataExchange.Converters.BaseItemModelConverter<TTo>, Sitecore.DataExchange``

+---------------------------+---------------------------------------------------------------------+
| Type                      | |type|                                                              |
+---------------------------+---------------------------------------------------------------------+

Example
---------------------------------------------------
Consider an example where you have a Sitecore template
that represents a person. The template has the following
fields:

+---------------------------+---------------------------------------------------------------------+
| Field name                | Field type                                                          |
+===========================+=====================================================================+
| Name                      | **Single-Line Text**                                                |
+---------------------------+---------------------------------------------------------------------+
| Email                     | **Single-Line Text**                                                |
+---------------------------+---------------------------------------------------------------------+
| DOB                       | **Date**                                                            |
+---------------------------+---------------------------------------------------------------------+

Within Data Exchange Framework you want items based on 
this template to be exposed using the following model:

.. code-block:: c#

    public class Person
    {
        public string Name { get; set; }
        public string Email { get; set; }
        public DateTime DateOfBirth { get; set; }
    }

The following class uses the base item model converter
to create an instance of the model above from a Sitecore
item based on the template above:

.. code-block:: c#

    using Sitecore.DataExchange.Attributes;
    using Sitecore.DataExchange.Repositories;
    using Sitecore.Services.Core.Model;

    namespace Examples
    {
        [SupportedIds(PersonTemplateId)]
        public class PersonConverter : BaseItemModelConverter<Person>
        {
            public const string PersonTemplateId = "[PERSON TEMPLATE ID]";
            public PersonConverter(IItemModelRepository repository) : base(repository)
            {
            }
            protected override ConvertResult<Person> ConvertSupportedItem(ItemModel source)
            {
                if (source == null)
                {
                    return ConvertResult<Person>.NegativeResult();
                }
                var person = new Person
                {
                    Name = base.GetStringValue(source, "Name"),
                    Email = base.GetStringValue(source, "Email"),
                    DateOfBirth = base.GetDateTimeValue(source, "DOB")
                }
                return ConvertResult<Person>.PositiveResult(person);
            }
        }
    }

.. note::

    The attribute ``SupportedIds`` is used for validation purposes.
    It ensures the converter can only be used with items based on
    the specified templates.