Mappings Applied Actions
==============================================

When a *value mapping set* is run, it is possible that data is changed.
In the event that data is changed, it may be useful to be able to
perform a task. A *mappings applied action* presents logic that
can be run in this situation.

.. note::

    Just because a mapping set is applied, it does not mean that the target object was
    actually changed. For example, consider a mapping set with a single mapping in it. The 
    mapping changes the name of the city that an xDB contact (the target object) lives in.

    What happens if the city name that the mapping set tries to apply is null? This means 
    there is no value to write to the target object. In this case, the mapping set *was*
    applied, but the xDB contact was not changed.

    So in this case, you probably do not want to save the xDB contact, because the 
    contact has not changed. There is no value in saving the contact.

    Now, you have hundreds of contacts you are updating in this way. Some of those 
    contacts will be updated and some will not. When a contact is updated, you might
    want to put the contract into a queue. After all of the contacts are updated, the
    queue will contain only those contacts that were changed.

    *Mapping applied actions* allow you to configure Data Exchange Framework to 
    put the contact in the queue if the contact is changed.

.. note::
    These templates are defined in the following location:

    **Templates > Data Exchange > Framework > Data Access > Mappings Applied Actions** 

.. toctree::
    :name: framework-mappings-applied-action-templates
    :caption: Templates 
    :titlesonly:
    :maxdepth: 2

    update-work-queue-entry-status

.. toctree::
    :name: framework-mappings-applied-action-base-templates
    :caption: Base Templates 
    :titlesonly:
    :maxdepth: 2

    base-mappings-applied-action
