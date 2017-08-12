Dynamics CRM Provider
=================================================

.. contents:: What's new in version 1.4.1
   :depth: 2
   :local:

Dynamics CRM Provider for Data Exchange Framework
----------------------------------------------------------

API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * :download:`Sitecore.Analytics.DynamicsCrm.dll <_static/Sitecore.Analytics.DynamicsCrm.dll 1.4.0 to 1.4.1.html>`

----------------------------------------------------------

Dynamics CRM Provider for CRM Connect
----------------------------------------------------------

.. note::
    Prior to version 1.4.1, CRM Connect expected that a CRM contact 
    could be associated with zero-to-many "marketing lists". While 
    it was safe to assume that, conceptually, this was true, the
    problem is that the term "marketing list" is hardly universal. 
    We realized this while implementing a provider a different CRM. 
    
    In order to avoid needless confusion, we made the decision to
    remove the marketing list property from the contact and leave
    it to the specific CRM implementation to determine the proper
    name for this component. This way, the implementation could 
    use the appropriate term.

    For Dynamics CRM, the appropriate term is "marketing list".

API changes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    * :download:`Sitecore.Analytics.DynamicsCrm.dll <_static/Sitecore.Analytics.DynamicsCrm.dll 1.4.0 to 1.4.1.html>`
