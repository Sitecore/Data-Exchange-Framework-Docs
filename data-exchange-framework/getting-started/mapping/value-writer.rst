Value Writer
=======================================

A *value writer* is a component that is able to write a value
to an object. Being able to write values is an essential part
of mapping values from the *source object* to the *target object*.

.. note::

    Data Exchange Framework includes a number of value writers.
    More information on those components is available in the
    :doc:`../../components/index` section, under 
    :doc:`../../components/framework/data-access/value-writers/index`.

In addition, custom value writers can be created by implementing 
the ``Sitecore.DataExchange.DataAccess.IValueWriter`` interface.

.. hint::

    If you are developing a custom provider, you may need to develop  
    custom value writers, but often this is not necessary. In many cases,
    the target object will have a property whose value must be set. Data
    Exchange Framework includes a value writer that can be used to do this.

    Sometimes the property on the target object will, itself, be an object, 
    and the value must be written to a property of this second object. 
    For example, the target object could be a person. The person has a 
    property that represents a collection of email addresses. You want to
    change the person's work email address.

    In this example, the target object is a person. The property on the 
    person is ``Emails``. The property on the ``Emails`` property is 
    ``Address``. Data Exchange Framework includes 
    :doc:`../../components/framework/data-access/value-writers/target-reader` 
    for this case.