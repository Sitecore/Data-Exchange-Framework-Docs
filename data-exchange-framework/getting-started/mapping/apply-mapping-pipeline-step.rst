Apply Mapping Pipeline Step
=======================================

Data Exchange Framework includes the ``Apply Mapping Pipeline Step``
*pipeline step*. The *pipeline step processor* assigned to this 
pipeline step implements the following logic:

    1. Read the *source* object from the *pipeline context*
    2. Read the *target* object from the pipeline context
    3. Read the *value mapping set* assigned to the pipelines step
    4. Apply the value mapping set specified on the property ``Mapping Set`` 
       on the pipeline step

The pipeline step processor requires a source object and a target 
object be set in the pipeline context using the 
``Sitecore.DataExchange.Plugins.SynchronizationSettings`` plugin. 
This plugin must be set up by a pipeline step processor that ran 
prior to this pipeline step processor. 

.. note::

    More information on this component is available in the
    :doc:`../../components/index` section, under 
    :doc:`../../components/framework/pipeline-steps/apply-mapping`.
