Add Processor to Resolve Language Versions
=================================================

In the previous step you specified which languages you intend 
to write to on the Sitecore item. Now you must add a 
*pipeline step* that is able to resolve the Sitecore item 
you want to update, along with the language versions that 
you selected.

1. Add the *pipeline step* :doc:`../../../components/sitecore/pipeline-steps/resolve-multilanguage-sitecore-item-dictionary` to your *pipeline*.

    .. note::
        Be sure to add this *pipeline step* after the step added in the previous step.

