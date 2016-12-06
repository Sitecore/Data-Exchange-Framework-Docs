Value Mapping
==========================================

This template is the base template for all *value mappings*.

.. include:: ../../../../../common/base-template-never-inherit-notice.txt

+-----------------+-----------------------------------------------------------+
| Template name   | **Value Mapping**                                         |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+---------------------------------+---------------------------------------------------------------+
| Field                           | Description                                                   |
+=================================+===============================================================+
| ``Source Accessor``             | | Value accessor that reads from the source object.           |
+---------------------------------+---------------------------------------------------------------+
| ``Target Accessor``             | | Value accessor that writes to the target object.            |
+---------------------------------+---------------------------------------------------------------+
| ``Source Value Transformer``    | | Value reader used to convert the value read from the        |
|                                 | | source object into a format that is compatible with         |
|                                 | | the target object.                                          | 
+---------------------------------+---------------------------------------------------------------+
| ``Ignore Null Values``          | | If ticked, if a null value is read by Source Accessor,      |
|                                 | | the value is not mapped.                                    |
|                                 | |                                                             |
|                                 | | This field can be used to ensure that existing values are   |
|                                 | | not overwritten by empty or null values.                    |
+---------------------------------+---------------------------------------------------------------+
| ``Apply Mapping Rules``         | | Rules that determine whether or not the value is mapped.    |
|                                 | | All of the selected rules must pass in order for the value  |
|                                 | | mapping to be used.                                         |
|                                 | |                                                             |
|                                 | | This field can be used to ensure that existing values are   |
|                                 | | overwritten only under certain conditions.                  |
+---------------------------------+---------------------------------------------------------------+



