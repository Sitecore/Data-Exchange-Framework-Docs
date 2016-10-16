Value Readers
=======================

As its name suggests, a *value reader* is able to read a value from 
an object. The object from which the value is read is called the
*source object*.

In many cases, the value reader reads the value from a source object 
exactly as the value exists on the source object. For example, you 
want to read the name of a contact.

But in other cases, the value reader must do more. For example, 
consider a case where a contact has a property that stores a 
collection of names (first name, surname, nickname, etc.)
You want to read a specific name. In this case, the value reader
would be able to determine which name you want to read.

And in other cases, the value reader can be used to transform 
values. For example, consider a case where you want to read the
contact's date of birth. The contact object returns a .NET ``DateTime``
object. But you need the value in a specific format: ``yyyy-MM-dd``.
A value reader can be used to read the ``DateTime`` and then 
convert that object to a string.

.. note::
    These templates are defined in the following location:

    **Templates > Data Exchange > Framework > Data Access > Value Readers** 

.. toctree::
    :name: framework-value-readers-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    array-value
    enum-value
    constant
    fallback
    iso-date
    method
    now
    property
    raw-value
    sequential
    value-accessor-value-reader

.. toctree::
    :name: framework-value-readers-base-templates
    :caption: Base Templates 
    :titlesonly:
    :maxdepth: 2

    base-value-reader
