Specify Languages to Read
==============================

Resolving the *source object* is a little more complex when dealing
with multiple languages. This is because you are actually reading
from multiple *source objects*. Data Exchange Framework hides most
of the technical details involved, but you do need to identify
the languages you are going to read.

1. In Content Editor, select the *pipeline* you want to update.
2. Add the *pipeline step* :doc:`../../../components/sitecore/pipeline-steps/select-languages` to your *pipeline*.
3. Select the pipeline step item.
4. In the field ``Languages``, select the languages you want to read from.

  .. hint::
    The languages that are available are defined in the Sitecore database under **/sitecore/system/Languages**.

5. Save the pipeline step item.