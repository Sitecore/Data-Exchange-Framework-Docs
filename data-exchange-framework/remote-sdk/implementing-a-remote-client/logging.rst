Logging
=======================================

Data Exchange Framework components write to a log that is accessed
from the following property:

``Sitecore.DataExchange.Context.Logger``

When using the remote API, the logger is set by default to be a null
logger. This logger ensures that a logger is available to framework
components, but it does not store any messages written to it.

In order to capture the information written to the log, you must set 
the logger. You must implement the logger yourself by implementing 
the following interface:

``Sitecore.Services.Core.Diagnostics.ILogger``
 