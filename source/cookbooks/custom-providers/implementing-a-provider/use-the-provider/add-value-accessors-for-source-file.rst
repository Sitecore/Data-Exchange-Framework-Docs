Add Value Accessors for Source File
===================================================
In order to read values from the source file, value accessors
are needed. Related value accessors are grouped into value
accessor sets. A value accessor set may contain one or more
value accessors. 

Each value accessor represents a specific value
from a row in the source file.

.. contents:: In this topic:
   :local:

Create Folder for Value Accessor Set
---------------------------------------------------
Under a tenant, value accessor sets are organized by provider. 
Each provider has its own folder. A folder is needed to hold
the value accessor sets for the new provider.

1. In Content Editor, select the tenant.

.. image:: _static/select-new-tenant.png

2. Navigate to **Data Access > Value Accessor Sets > Providers**

.. image:: _static/value-accessor-sets-providers.png

3. Add the following item:

+---------------------------+---------------------------------------------------------------------+
| Template                  | **File System Value Accessor Sets**                                 |
+---------------------------+---------------------------------------------------------------------+

.. hint::

    This template is a command template. It does not prompt 
    for the item name. The command template assigns the item 
    name automatically.

4. Select the new item.

.. image:: _static/file-system-provider-value-accessor-sets.png

Create Value Accessor Set
---------------------------------------------------
Next, you need to create a value accessor set that represents
all of the values you want to read from a row in the source file.

1. Add the following item:

+---------------------------+---------------------------------------------------------------------+
| Template                  | **Array Value Accessor Set**                                        |
+---------------------------+---------------------------------------------------------------------+
| Item name                 | **City Information File Fields**                                    |
+---------------------------+---------------------------------------------------------------------+

2. Select the new item.

.. image:: _static/city-information-file-fields-value-accessor-set.png

Create Value Accessors
---------------------------------------------------
For each value you want to read from a row in the source file
you need a separate value accessor. When a row is read from 
the source file, it is split into an array. Each value 
accessor represents a position in that array.

1. Add the following item:

+---------------------------+---------------------------------------------------------------------+
| Template                  | **Array Value Accessor**                                            |
+---------------------------+---------------------------------------------------------------------+
| Item name                 | **Identifier from City Information File**                           |
+---------------------------+---------------------------------------------------------------------+

2. Select the new item.

.. image:: _static/identifier-for-file.png

3. Set the following field values:

+---------------------------+---------------------------------------------------------------------+
| Field                     | Value                                                               |
+===========================+=====================================================================+
| Position                  | **0**                                                               |
+---------------------------+---------------------------------------------------------------------+

4. Save the item.

5. Select the item **City Information File Fields**.

.. image:: _static/city-information-file-fields-value-accessor-set-with-1-accessor.png

6. Add the following item:

+---------------------------+---------------------------------------------------------------------+
| Template                  | **Array Value Accessor**                                            |
+---------------------------+---------------------------------------------------------------------+
| Item name                 | **Country from City Information File**                              |
+---------------------------+---------------------------------------------------------------------+

7. Select the new item.

.. image:: _static/country-for-file.png

8. Set the following field values:

+---------------------------+---------------------------------------------------------------------+
| Field                     | Value                                                               |
+===========================+=====================================================================+
| Position                  | **1**                                                               |
+---------------------------+---------------------------------------------------------------------+

9. Save the item.

10. Select the item **City Information File Fields**.

.. image:: _static/city-information-file-fields-value-accessor-set-with-2-accessors.png

11. Add the following item:

+---------------------------+---------------------------------------------------------------------+
| Template                  | **Array Value Accessor**                                            |
+---------------------------+---------------------------------------------------------------------+
| Item name                 | **City from City Information File**                                 |
+---------------------------+---------------------------------------------------------------------+

12. Select the new item.

.. image:: _static/city-for-file.png

13. Set the following field values:

+---------------------------+---------------------------------------------------------------------+
| Field                     | Value                                                               |
+===========================+=====================================================================+
| Position                  | **2**                                                               |
+---------------------------+---------------------------------------------------------------------+

14. Save the item.

