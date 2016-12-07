CRM Entity Repositories
=======================================

An *entity repository* is the component that is used to interact with a 
specific type of CRM entities. An *entity repository set* is a collection
of the entity repositories that are available on a specific CRM.

An entity repository provides a layer of abstraction between the 
Dynamics CRM API used to access entities, and the entities themselves.
For example, reading a list of CRM marketing lists is done the same  
way reading a list of CRM accounts. 

However, you also need a way to read the contacts that are assigned 
to a marketing list is different from the way you read the contacts
that are assigned to an account. But in Dynamics CRM Connect, you
get the ability to read both the list of entities and the members
in a consistent way. This is the purpose of the entity repository: 
to simplify access to entities. 

In addition, the entity repository makes it possible for a developer
to override the logic used to interact with a specific type of CRM
entity. For example, if you have optimized code you want to use to
read marketing list membership, you can override the entity repository
that is used to interact with marketing list membership so that your
optimized code is used.

.. note::

    These templates are defined in the following location:

    **Templates > Data Exchange > Providers > Dynamics CRM > Repositories** 

.. toctree::
    :name: dynamics-crm-provider-entity-repositories-templates
    :caption: Templates
    :titlesonly:
    :maxdepth: 2

    base-entity-repo
    xrm-client
    entity-repo-set

    