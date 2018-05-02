Method Value Reader
===================================================
This value reader invokes a method on the source object 
and returns the method's return value.

Method parameters are represented as children of the 
method value reader.

.. |source-type-label| replace:: Expected source object type
.. |source-type| replace:: ``System.Object``
.. |template-location| replace:: **Data Exchange > Framework > Data Access > Value Readers > Method Value Reader**

+---------------------------+---------------------------------------------------------------------+
| |source-type-label|       | |source-type|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Template location         | |template-location|                                                 |
+---------------------------+---------------------------------------------------------------------+

Template Fields
---------------------------------------------------

.. |method-name| replace:: Name of the method on the source object that is invoked.
.. |is-extension-method| replace:: If ticked, the method is expected to be an extension method on the source object.
.. |extension-method-type| replace:: Type name of the class that implements the extension method.

+---------------------------+---------------------------------------------------------------------+
| Field name                | Description                                                         |
+===========================+=====================================================================+
| Method Name               | |method-name|                                                       |
+---------------------------+---------------------------------------------------------------------+
| Is Extension Method       | |is-extension-method|                                               |
+---------------------------+---------------------------------------------------------------------+
| Extension Method Type     | |extension-method-type|                                             |
+---------------------------+---------------------------------------------------------------------+
