Implement Data Access Components
===================================================
Data access components represents logic used to read, 
write and map values during a data synchronization 
process. In this example, data access components 
represent the ability to read values at specific
positions from a line in a text file.

To be more specific, consider a file that contains
comma-separated values (CSV) that provide details
about new customers. The file looks like the following::

    first,last,company
    Aaron,Adkins,Ace Corp
    Brad,Bedford,Burnside Bread
    Charlotte,Colson,Carefree Farms

The pipeline step processor **ReadTextFileStepProcessor**
reads each row from a file and creates an array of
values using the specified delimiter. In this example, 
the delimiter is a comma.

Data access components are needed to access
how to access the values in that array. In 
this example, data access components are used
to identify the following:

    * first name is at position 1
    * last name (surname) is at position 2
    * company name is at position 3

This section covers how to implement the required 
data access components.

.. toctree::
   :maxdepth: 1

   create-template-for-value-accessor.rst
   implement-value-accessor-converter.rst
   set-default-values-on-value-accessor-template.rst
   create-template-for-value-accessor-set.rst
   set-default-values-on-value-accessor-set-template.rst