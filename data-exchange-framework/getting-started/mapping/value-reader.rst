Value Reader
=======================================

A *value reader* is a component that is able to read a value
from an object. Being able to read values is an essential part
of mapping values from the *source object* to the *target object*.

Sometimes the value that is read comes directly from the source 
object. For example, if the source object represents a contact 
from a CRM, you might want to read the contact's name of work
phone number.

In other cases, the value isn't read from the source object. 
For example, you might want to write the current date to
the target object. You need a component that is able to 
*read* the current date. 

.. note::

    Data Exchange Framework includes a number of value readers.
    More information on those components is available in the
    :doc:`../../components/index` section, under 
    :doc:`../../components/framework/data-access/value-readers/index`.

In addition, custom value readers can be created by implementing 
the ``Sitecore.DataExchange.DataAccess.IValueReader`` interface.

.. hint::

    If you are developing a custom provider, it is likely you will 
    develop custom value readers. For example, the Dynamics CRM provider
    includes a value reader that can read a property from a CRM entity. 