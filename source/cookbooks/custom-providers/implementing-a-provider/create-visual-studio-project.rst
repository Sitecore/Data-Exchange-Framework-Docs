Create Visual Studio Project
===================================================
A Visual Studio project is needed before you can 
implement the data mapping logic.

1. In Visual Studio, create the following project:

+---------------------------+-------------------------------------------------+
| Project type              | Class Library (.NET Framework)                  |
+---------------------------+-------------------------------------------------+
| .NET version              | .NET Framework 4.6.2                            |
+---------------------------+-------------------------------------------------+
| Project name              | ``Examples.DataExchange.Providers.FileSystem``  |
+---------------------------+-------------------------------------------------+

2. Add references to the following NuGet packages:

    * ``Sitecore.DataExchange.DataAccess.NoReferences``
    * ``Sitecore.DataExchange.NoReferences``
    * ``Sitecore.Services.Core.NoReferences``

.. |link-for-nuget-feed| raw:: html

   <a href="https://sitecore.myget.org/gallery/sc-packages" target="_blank">https://sitecore.myget.org/gallery/sc-packages</a>

.. note::

    Sitecore's public NuGet feed is available at |link-for-nuget-feed|.