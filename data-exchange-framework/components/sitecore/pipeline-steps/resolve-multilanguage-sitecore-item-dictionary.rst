Resolve Multilanguage Sitecore Item Dictionary
=================================================

This *pipeline step* is used to resolve a dictionary of Sitecore 
``ItemModel`` objects. The key in the dictionary is an instance
of ``CultureInfo``.

The entries in the dictionary depend on the languages available
in the *pipeline context plugin* ``SelectedLanguagesSettings``.
This plugin is set by the pipeline step :doc:`select-languages`.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Resolve Multilanguage Sitecore Item Dictionary Pipeline Step**      |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../sitecore/pipeline-steps/resolve-sitecore-item`            |
+-----------------------------------+-----------------------------------------------------------------------+

.. include:: ../../../../common/no-template-fields-added.txt

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``SelectedLanguagesSettings``     | | This pipeline step resolves specific language versions of a         |
|                                   | | Sitecore item. This plugin determines which languages to retrieve.  |
+-----------------------------------+-----------------------------------------------------------------------+
