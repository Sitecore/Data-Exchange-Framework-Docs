Contact Facet Property (Indexer)
==========================================

This *value accessor* is used for "dictionary properties". A dictionary 
property is a property on a contact facet that stores multiple values, 
where each value is identified by a key.

For example, email addresses are stored in a dictionary property, 
because a contact might have a work email address, home email address 
and a backup email address. In this example, the keys might be "work", 
"home" and "other".

Other values that are stored in dictionary properties are addresses 
and telephone numbers.

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **xDB Contact Facet Indexer Property Value Accessor**                 |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`contact-facet-property`                                         |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Contact facet name``                        | | Name of the contact facet to access.                    |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Property name of indexer property``         | | Name of the property on the contact facet that is       |
|                                               | | an indexer property.                                    |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Index name for indexer property``           | | Name of the key in the dictionary used to store the     | 
|                                               | | specific value.                                         |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Property name``                             | | Name of the property on the object read from the        | 
|                                               | | dictionary whose value is accessed.                     |
+-----------------------------------------------+-----------------------------------------------------------+

