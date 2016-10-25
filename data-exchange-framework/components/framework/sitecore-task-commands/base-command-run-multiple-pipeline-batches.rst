Base Run Multiple Pipeline Batches Command
======================================================

This template is the base template for all commands that involve 
running multiple *pipeline batches*.

+-----------------+-----------------------------------------------------------+
| Template name   | **Base Run Multiple Pipeline Batches Command**            |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

+-----------------------------------------------+-----------------------------------------------------------+
| Field                                         | Description                                               |
+===============================================+===========================================================+
| ``Abort If Pipeline Batch Already Running``   | | If ticked, this setting ensures a pipeline batch        |
|                                               | | cannot run multiple times concurrently.                 |
|                                               | |                                                         |
|                                               | | It should be assumed that it is not safe to run a       |
|                                               | | pipeline batch multiple times concurrently on a single  |
|                                               | | Sitecore server.                                        |
|                                               | |                                                         |
|                                               | | This option should only be disabled if you are certain  | 
|                                               | | the selected pipeline tasks can run multiple times      |
|                                               | | concurrently.                                           |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Continue On Error``                         | | If ticked and an error occurs while a pipeline batch    |
|                                               | | is running, subsequent pipeline batches will be run.    |
|                                               | |                                                         |
|                                               | | If unticked and an error occurs while a pipeline batch  |
|                                               | | is running, no subsequent pipeline batches will be      |
|                                               | | run.                                                    |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Use Asynchronous Mode``                     | | If ticked, pipeline batches will be run asynchronously. |
|                                               | |                                                         |
|                                               | | If unticked, pipeline batches are run serially, with    |
|                                               | | each pipeline batch being started after the previous    |
|                                               | | pipeline batch has finished.                            |
+-----------------------------------------------+-----------------------------------------------------------+
| ``Pipeline Batch Runner Type``                | | The .NET type that implements the logic to run the      |
|                                               | | pipeline batches assigned to the command.               |
+-----------------------------------------------+-----------------------------------------------------------+
