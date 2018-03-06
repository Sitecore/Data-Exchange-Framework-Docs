Data Mapping Using Code
===================================================
When using Data Exchange Framework, the standard approach
for mapping data is to configure the mapping in the *tenant*.
In many cases, this approach works well because it reduces
the amount of custom code needed. Specific mappings can be
added or removed as needed, without having to write any code.

But there are cases where the mapping logic is too complex
to be described through configuration. And there are cases
where existing data mapping logic should be reused. In 
these cases, you need to be able to define data mapping
using code.

This section describes how to build, deploy and integrate 
the components needed to implement code-based data mapping.

.. toctree::
   :maxdepth: 1

   create-visual-studio-project.rst
   implement-custom-value-mapping-set.rst
   create-template-for-custom-value-mapping-set.rst
   implement-converter-for-custom-value-mapping-set.rst
   integrate-custom-value-mapping-set.rst