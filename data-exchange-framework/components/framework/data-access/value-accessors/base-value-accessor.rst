Base Value Accessor
==========================================

This *value accessor* allows a value reader and/or value writer 
to be set explicitly. 

.. include:: ../../../../../common/base-template-always-inherit-notice.txt

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Value Accessor**                                                    |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | none                                                                  |
+-----------------------------------+-----------------------------------------------------------------------+

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Value Reader``                  | | Value reader used to read a value.                                  |
|                                   | |                                                                     |
|                                   | | Most templates that inherit from this template use other fields to  |  
|                                   | | provide information that is used to automatically determine the     |
|                                   | | appropriate value reader.                                           |
|                                   | |                                                                     |
|                                   | | This field makes it possible for the value reader on a specific     |
|                                   | | item to be set explicitly. This field is not used often.            |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Value Writer``                  | | Value writer used to write a value.                                 |
|                                   | |                                                                     |
|                                   | | Most templates that inherit from this template use other fields to  |  
|                                   | | provide information that is used to automatically determine the     |
|                                   | | appropriate value reader.                                           |
|                                   | |                                                                     |
|                                   | | This field makes it possible for the value reader on a specific     |
|                                   | | item to be set explicitly. This field is not used often.            |
+-----------------------------------+-----------------------------------------------------------------------+
