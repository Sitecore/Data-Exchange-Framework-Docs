Using Nullable Types
==========================

When synchronizing data, it is important that you understand the 
values being read and being written. One scenario that you must 
consider carefully is when you are reading nullable types.

Consider a case where you are mapping data from a contact in xDB 
to a contact in Dynamics CRM. In xDB, the contact has a property
on a facet that represents the contact's date of birth. 

On the contact facet, the date of birth is defined as ``DateTime?``,
which is a nullable ``DateTime``. This makes it possible for no
date of birth to be specified (meaning the property is null).

As a developer, when you work with nullable type values, you 
use them the same way you use value types. For example:

.. code-block:: c#

    DateTime? now = DateTime.Now;
    if (now > new DateTime(2017, 1, 1))
    {
        //do something
    }

But a more accurate view of what is going on is the following,
because this more closely reflects the code after it is compiled:

.. code-block:: c#

    DateTime? now = new DateTime?(DateTime.Now);
    if (now.Value > new DateTime(2017, 1, 1))
    {
        //do something
    }

This has a significant impact within Data Exchange Framework.
The framework uses reflection for most of its mapping operations.
Reflection works on the compiled code, not the source code.

This means that when you are using nullable types with framework
components, you must use the ``Value`` property.

So, to continue the example, if you want to use the xDB contact's
date of birth as a source value in a mapping, you cannot simply
point to the property on the contact facet. That will give you
access to a ``DateTime?``. You must read the ``Value`` property
from the ``DateTime?`` object.

The field "Source Value Transformer" on the Value Mapping template was designed for this situation.

1.	In Content Editor, select your tenant.
2.	Navigate to **Data Access > Value Readers > Common**.
3.	Create a new item using the template **Property Value Reader**.
4.	Select the new item.
5.	For the field **Property Name**, set the value to be "Value".
6.	Save the item.
7.	Navigate to the Value Mapping item that represents the mapping of the xDB date to the CRM date.
8.	For the field **Source Value Transformer**, select the item you created in step 3.
9.	Save the item.
