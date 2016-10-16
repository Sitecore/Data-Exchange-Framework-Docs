Value Accessors
=======================

A *value accessor* associates the component used to read a value 
(*value reader*) with the component used to write a value (*value writer*).

The following comparison might be helpful:

+-------------------------+------------------+
| Data Exchange Framework | C#               |
+=========================+==================+
| Value accessor          | Property         |
+-------------------------+------------------+
| Value reader            | Property getter  |
+-------------------------+------------------+
| Value writer            | Property setter  |
+-------------------------+------------------+

Value accessors are used to configure *value mappings*. One value 
accessor identifies the component used to read a value from the 
source object, and another value accessor identifies the component
used to write a value to the target object.

.. note::
    These templates are defined in the following location:

    **Templates > Data Exchange > Framework > Data Access > Value Accessors** 

.. toctree::
    :name: framework-value-accessor-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    property

.. toctree::
    :name: framework-value-accessor-base-templates
    :caption: Base Templates 
    :titlesonly:
    :maxdepth: 2

    base-value-accessor
