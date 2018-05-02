Converters
===================================================
When a developer creates a custom component for Data 
Exchange Framework, he will usually need to create a
template to represent the component. A converter is
needed to transform items based on the template into
a format that is compatible with Data Exchange Framework.

Converters are implemented in code. This section 
describes the base classes developers can use to
simplify the task of creating custom converters.

.. toctree::
   :maxdepth: 1

   base-item-model-converter.rst
   base-endpoint-converter.rst
   base-pipeline-step-converter.rst

.. note::

    You may be wondering why Data Exchange Framework
    provides its own object mapping implementation
    instead of using an existing tool like `Glass.Mapper <http://glass.lu/Mapper/>`_. 

    The reason is that these tools typically are designed
    to run on a Sitecore server and have a dependency on 
    the Sitecore kernel. Data Exchange Framework aims to
    avoid these requirements. Therefore it implements its
    own lightweight and specialized functionality.