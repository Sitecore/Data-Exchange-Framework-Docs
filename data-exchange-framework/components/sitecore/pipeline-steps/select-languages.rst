Select Languages
=============================

This *pipeline step* is used to specify Sitecore languages that 
are used in subsequent pipeline steps.

This pipeline step does very little. It merely collects a list
of languages that other pipeline steps can use. One example is
:doc:`resolve-multilanguage-sitecore-item-dictionary`.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Select Languages Pipeline Step**                                    |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+


+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Languages``                     | | The selected languages are added to the plugin                      |
|                                   | | ``SelectedLanguagesSettings``, so that subsequent pipeline steps    |
|                                   | | can use them.                                                       |
+-----------------------------------+-----------------------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``SelectedLanguagesSettings``     | | Provides access to the languages that will be used to read          |
|                                   | | or write content to Sitecore items.                                 |
+-----------------------------------+-----------------------------------------------------------------------+
