Mapping
=======================================

Data Exchange Framework includes components that allow data to
be mapped between objects. The goal of these components is to
remove the need for custom development when mapping data 
between systems.  

Mapping typically involves the following process:

    1. *Pipeline step processor* reads data. This is the *source* object.
    2. Pipeline step processor resolves the object to write data to. 
       This is the *target* object. 
    3. Pipeline step processor applies a set of mappings to the target object.  

Mapping is configured using the following components: 

.. toctree::
    :maxdepth: 2
    :titlesonly:

    value-reader
    value-writer
    value-accessor
    value-accessor-set
    value-mapping
    value-mapping-set
    apply-mapping-pipeline-step
