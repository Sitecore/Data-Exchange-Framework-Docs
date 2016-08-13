Tenant
=======================================

A *tenant* is a component that encapsulates all of the components
that are used to define synchronization processes for a specific
brand or organization.

On a single Sitecore server you can create as many tenants as you like.
Each tenant maintains its own configuration. This means each tenant
maintains its own:

    * *Endpoints*
    * *Pipeline batches*
    * *Pipelines*
    * *Value accessor sets*
    * *Value mapping sets*

Furthermore, these components are not shared between tenants.

There are many reasons for having multiple tenants on a single 
Sitecore server:

    * **Multiple brands synchronize data between different systems.**
      Separate tenants allow you to keep the synchronization 
      processes in one brand separate from another brand. 
    * **Data from multiple systems is synchronized.** The configuration
      for these systems is complicated, and is maintained by different
      people. Having separate tenants allows the administrators to 
      change their tenant without affecting other administrators.
    * **New configurations need to be tested in isolation.** Having
      a separate tenant where new configurations can be tested means
      the current configuration does not need to be changed.