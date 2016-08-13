Add Value Accessor Set for Source
===========================================================

The source object is a row of data from the text file. The 
*value accessor set* defines the values that are available
in the row.

First you must create the folder into which the value accessor set
can be added.

1. Navigate to your tenant.
2. Navigate to **Data Access > Value Accessor Sets > Providers**.
3. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **File System Value Accessor Sets Root**                            |
    +-------------------+---------------------------------------------------------------------+

    .. hint:: 
    
        This template is a command template. It does not prompt for the 
        item name. The command template assigns the item name automatically.

The new value accessor sets folder in Content Editor.

.. image:: _static/file-system-value-accessor-sets-root.png

Next you must add a value accessor set to the folder.

4. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Array Value Accessor Set**                                        |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **City Information File Fields**                                    |
    +-------------------+---------------------------------------------------------------------+

5. Set the following field values:

    +---------------------------------+---------------------------------------------------------------------+
    | Field                           | Value                                                               |
    +=================================+=====================================================================+
    | Path                            | **C:\\Sitecore\\cities.dat**                                        |
    +---------------------------------+---------------------------------------------------------------------+
    | Column separator                | **,**                                                               |
    +---------------------------------+---------------------------------------------------------------------+
    | Column headers in first line    | **ticked**                                                          |
    +---------------------------------+---------------------------------------------------------------------+

The new value accessor set in Content Editor.

.. image:: _static/value-accessor-set-for-source.png

Next you must add *value accessor* items to the value accessor set.

6. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Array Value Accessor**                                            |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **Identifier**                                                      |
    +-------------------+---------------------------------------------------------------------+

7. Set the following field values:

    +---------------------------------+---------------------------------------------------------------------+
    | Field                           | Value                                                               |
    +=================================+=====================================================================+
    | Position                        | **1**                                                               |
    +---------------------------------+---------------------------------------------------------------------+

8. Save the item.
9. Navigate back to the value accessor set item.
10. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Array Value Accessor**                                            |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **Country**                                                         |
    +-------------------+---------------------------------------------------------------------+

11. Set the following field values:

    +---------------------------------+---------------------------------------------------------------------+
    | Field                           | Value                                                               |
    +=================================+=====================================================================+
    | Position                        | **2**                                                               |
    +---------------------------------+---------------------------------------------------------------------+

12. Save the item.
13. Navigate back to the value accessor set item.
14. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Array Value Accessor**                                            |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **City**                                                            |
    +-------------------+---------------------------------------------------------------------+

15. Set the following field values:

    +---------------------------------+---------------------------------------------------------------------+
    | Field                           | Value                                                               |
    +=================================+=====================================================================+
    | Position                        | **3**                                                               |
    +---------------------------------+---------------------------------------------------------------------+

16. Save the item.

The new value accessors in Content Editor.

.. image:: _static/file-system-value-accessors.png

