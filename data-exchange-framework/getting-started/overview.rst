Overview
=======================================

Data Exchange Framework is designed to facilitate the transfer 
of data between two systems. 

The system being read from is called the *source* system. 
The system being written to is called the *target* system.

Data Exchange Framework allows you to do things like:

+-------------------------------------------------------------------+-----------+-----------+
| Example                                                           | Source    | Target    |
+===================================================================+===========+===========+
| Read contacts from a CRM and create contacts in xDB               | CRM       | Sitecore  |
+-------------------------------------------------------------------+-----------+-----------+
| Update a contact in CRM using information from a contact in xDB   | Sitecore  | CRM       |
+-------------------------------------------------------------------+-----------+-----------+
| Create items in Sitecore that represent products in a catalog     | PIM       | Sitecore  |
+-------------------------------------------------------------------+-----------+-----------+

.. hint:: 

    Typically, either the source system or the target system is 
    Sitecore. However, Data Exchange Framework can be used to 
    transfer data between *any* two systems.
