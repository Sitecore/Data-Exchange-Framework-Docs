Pipeline Batch
==========================================

This *pipeline batch* represents any kind of pipeline batch.

.. include:: ../../../../common/base-template-never-inherit-notice.txt

+-----------------+-----------------------------------------------------------+
| Template name   | **Pipeline Batch**                                        |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Pipelines``                                 | | The value accessor that is used to read the value of    |
|                                               | | an attribute from an entity.                            |
|                                               | |                                                         |
|                                               | | It is important that the value accessor selected has    |
|                                               | | a field that identifies the attribute name. The         |
|                                               | | attribute name is used to build the filter for the      |
|                                               | | API call to Dynamics CRM.                               |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Requested At``                              | | The date/time that the pipeline batch was last started. |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Last Run Finished``                         | | The date/time that the pipeline batch last finished     |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Last Run Completed``                        | | If ticked, the last time the pipeline batch ran, it     |
|                                               | | finished (meaning no critical error occurred).          |
|                                               | |                                                         |
|                                               | | If unticked, the last time the pipeline batch ran, it   |
|                                               | | did not finish (meaning a critical error occurred       |
|                                               | | that prevented the pipeline batch from completing.      |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Messages``                                  | | Log messages that were captured from the last time the  |
|                                               | | pipeline batch ran.                                     |
|                                               | |                                                         |
|                                               | | These may also appear in the Sitecore log.              |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Log Levels``                                | | The values that are selected here determine what is     |
|                                               | | written to the ``Messages`` field.                      |
|                                               | |                                                         |
|                                               | | This setting does not affect the Sitecore log settings, |
|                                               | | and is not affected by the Sitecore log settings.       |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Max Size``                                  | | The maximuim number of messages that are written to     |
|                                               | | to the ``Messages`` field. Use -1 to indicate an        |
|                                               | | an unlimited number of messages are written.            |
|                                               | |                                                         |
|                                               | | This setting does not affect the Sitecore log settings, |
|                                               | | and is not affected by the Sitecore log settings.       |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Can Run Out of Process``                    | | If ticked, it indicates this pipeline batch can be run  |
|                                               | | from outside of the Sitecore server.                    |
|                                               | |                                                         |
|                                               | | By detault this field is unticked. If you enable this   |
|                                               | | setting you must make sure all of the pipeline steps    |
|                                               | | included in each of the pipelines assigned to this      |
|                                               | | pipeline batch can be run in this way.                  |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Elevated Security User Name``               | | A user name that is available to any pipeline step that |
|                                               | | is run as a part of this pipeline batch.                |
|                                               | |                                                         |
|                                               | | The pipeline step may use this value however it likes.  |
|                                               | | This setting does nothing more than provide a value     |
|                                               | | that can be used, if appropriate.                       |
+-----------------------------------------------+-----------------------------------------------------------+
