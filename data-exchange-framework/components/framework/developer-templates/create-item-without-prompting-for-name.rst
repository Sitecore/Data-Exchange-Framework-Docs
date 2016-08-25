Create Item Without Prompting for Name
=======================================

This branch template allows you to ensure that a new item with a 
specific name is created.

This is important when you create a custom provider. Building a 
provider involves creating a number of templates and assigning
appropriate insert options. Often times it is important that 
vertain items (such as folders) have a specific item name.
This command template makes it possible to enfore a naming 
policy.   

+-----------------+-----------------------------------------------------------+
| Template name   | **Create Item Without Prompting for Name Branch**         |
+-----------------+-----------------------------------------------------------+
| Base template   | none                                                      |
+-----------------+-----------------------------------------------------------+

Child Items
---------------------------------------

The branch template has a command template as a child item. The command 
template uses its own child item to determine what kind of item to create.

+----------------------------------------+------------------------------------------------------------------+
| Field                                  | Description                                                      |
+========================================+==================================================================+
| ``Name for new item``                  | When the new item is created, this is the name that is used.     |
+----------------------------------------+------------------------------------------------------------------+
| ``Template for new item``              | When the new item is created, this is the template that is used. |
+----------------------------------------+------------------------------------------------------------------+

