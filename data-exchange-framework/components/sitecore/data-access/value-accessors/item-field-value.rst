Item Field Value
==========================================

This *value accessor* is used to access a field value on a Sitecore item.

+-----------------------------------+---------------------------------------------------------------------------------+
| Template name                     | **Sitecore Item Field Value Accessor**                                          |
+-----------------------------------+---------------------------------------------------------------------------------+
| Base template                     | :doc:`../../../framework/data-access/value-accessors/base-value-accessor`       |
+-----------------------------------+---------------------------------------------------------------------------------+

.. |reading| replace:: :doc:`../../../../cookbooks/synchronization/reading-multilanguage-content-from-sitecore-items/index`
.. |writing| replace:: :doc:`../../../../cookbooks/synchronization/writing-multilanguage-content-to-sitecore-items/index`

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Field``                         | | Field on a Sitecore template whose value is accessed.               |
+-----------------------------------+-----------------------------------------------------------------------+
| ``Language``                      | | The field value is accessed from this language.                     |
|                                   | |                                                                     |
|                                   | | This field is optional. However, if the field is used you must      |
|                                   | | modify your *pipeline* to include the required *pipeline steps*.    |
|                                   | |                                                                     |
|                                   | | For more information see the following sections:                    |
|                                   | |   * |reading|                                                       |
|                                   | |   * |writing|                                                       |
+-----------------------------------+-----------------------------------------------------------------------+
