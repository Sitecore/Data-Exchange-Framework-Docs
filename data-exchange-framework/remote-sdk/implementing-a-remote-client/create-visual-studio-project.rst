Create Visual Studio Project
=======================================

A Visual Studio project is needed for the console application.

1. In Visual Studio, create the following project:

    +---------------------------------+---------------------------------------+
    | Template                        | **Console Application**               |
    +---------------------------------+---------------------------------------+
    | Name                            | **Examples.RemoteManager**            |
    +---------------------------------+---------------------------------------+
    | .NET Framework version          | **4.5.2 (or higher)**                 |              
    +---------------------------------+---------------------------------------+

2. Add references to the following assemblies:

    * **Sitecore.DataExchange**
    * **Sitecore.DataExchange.DataAccess**
    * **Sitecore.DataExchange.Remote**
    * **Sitecore.Services.Core**

3. Replace **Program.cs** with the following:

    .. code-block:: c#
    
    .. important:: 

        Replace **[SITECORE HOST]** with the host name of the Sitecore server
        you want to connect to. For example, ``sc82.localhost``.

        Replace **[SITECORE USER]** with your Sitecore user name, including
        the domain. For example, ``sitecore\\admin``.

        Replace **[SITECORE PASSWORD]** with the password for the Sitecore user.

        Replace **[DATABASE NAME]** with the name of the Sitecore database
        you want to read configuration from.

    .. important:: 
    
        The Sitecore server must have Sitecore Item Web API enabled. This
        means the following must be configured:

            * The Sitecore configuration setting **itemwebapi.mode** must 
              be set to something other than ``Off``
            * SSL must be enabled on IIS



