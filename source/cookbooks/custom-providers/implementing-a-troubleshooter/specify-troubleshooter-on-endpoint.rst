Specify Troubleshooter on Endpoint
===================================================
A troubleshooter can be specified on any item that 
inherits from the Data Exchange Framework templates 
**Convertible** and **Troubleshootable**. 

In this example, the troubleshooter is being added 
to the text file endpoint, which inherits from the 
template **Base Endpoint**, which meets the criteria,
so no additional work is needed.

1. In Sitecore, open Content Editor.
2. Navigate to **sitecore > templates > Data Exchange > Providers > File System > Endpoints > Text File Endpoint > __Standard Values**
3. Set the following field values:

.. |field1-name| replace:: Troubleshooter Type
.. |field1-value| replace:: **Examples.DataExchange.Providers.FileSystem.TextFileEndpointTroubleshooter, Examples.DataExchange.Providers.FileSystem**

+---------------------------+---------------------------------------------------------------------+
| Field                     | Value                                                               |
+===========================+=====================================================================+
| |field1-name|             | |field1-value|                                                      |
+---------------------------+---------------------------------------------------------------------+

4. Save the item.


