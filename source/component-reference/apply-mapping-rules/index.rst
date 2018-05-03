Apply Mapping Rules
===================================================
An apply mapping rule is a component that determines 
whether a mapping should be applied. These components
allow you to configure the specific conditions that
must exist in order for data to be mapped.

For example, if you are mapping contact data between
two systems, the target system may require an email 
address for the contact. If you do not provide an
email address, you cannot create a contact in the 
target system. An apply mapping rule can be used
to describe this condition so that data is not 
mapped if an email address is missing.

.. toctree::
   :maxdepth: 1

   framework/index.rst
   salesforce/index.rst

