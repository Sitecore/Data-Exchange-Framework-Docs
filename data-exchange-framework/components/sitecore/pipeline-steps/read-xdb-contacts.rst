Read xDB Contacts
=============================

This *pipeline step* is used to read contacts from Sitecore xDB.

.. important:: 

    This pipeline step uses the Sitecore analytics index to read 
    xDB contacts. This means that contacts in MongoDB that have 
    not yet been indexed will not be included in the set of 
    contacts that are read by this pipeline step.

Template Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Template name                     | **Read xDB Contacts Pipeline Step**                                   |
+-----------------------------------+-----------------------------------------------------------------------+
| Base template                     | :doc:`../../framework/pipeline-steps/base-pipeline-step`              |
+-----------------------------------+-----------------------------------------------------------------------+

.. |endpoint| replace:: :doc:`../endpoints/index`

+-----------------------------------+-----------------------------------------------------------------------+
| Field                             | Description                                                           |
+===================================+=======================================================================+
| ``Endpoint From``                 | The Sitecore `endpoint <../endpoints/>`_ used to read xDB contacts.   |
+-----------------------------------+-----------------------------------------------------------------------+

Plugin Information
-----------------------------

+-----------------------------------+-----------------------------------------------------------------------+
| Plugin type                       | Description                                                           |
+===================================+=======================================================================+
| ``IterableDataSettings``          | | Subsequent pipeline steps use this plugin to access the contacts    |
|                                   | | read from xDB.                                                      |
|                                   | |                                                                     |
|                                   | | This step adds this plugin to the pipeline context.                 |
+-----------------------------------+-----------------------------------------------------------------------+
