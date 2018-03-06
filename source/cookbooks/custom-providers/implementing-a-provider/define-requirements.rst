Define Requirements
===================================================
The first thing you must do is define the requirements 
for your provider.

The following user stories describe how someone responsible 
for building and managing synchronization processes wants 
to be able to use text files:

#. **I can specify a file to read from** so that I can control which data is read.
#. **I can specify whether or not the file contains a header row** so that the provider does not impose constraints on the files it can read.
#. **I can specify a limit to the number of rows to read from the file** so that I can control the data that is read.
#. **I can map the value from a column in the file to a field on a Sitecore item** so I can populate Sitecore using data from the file.