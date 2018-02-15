Overview
===================================================
Within a synchronization process, a step may exist that 
handles the mapping of data from one object to another.

In Data Exchange Framework, a synchronization process 
is modeled in a *pipeline*. A pipeline is made up of 
*pipeline steps*. A specific type of *pipeline step*, 
:doc:`apply-mappings-pipeline-step`, is used to 
control the mapping of data.

.. contents:: In this topic:
   :local:

Components Used by the Pipeline Step
---------------------------------------------------
The pipeline step *Apply Mappings* involves the following components:

    * **Source object** - the object data is read from
    * **Target object** - the object data is written to
    * **Value mapping set** - instructions that specify what to read from the source object and what to write to the target object

Settings Configured on the Pipeline Step
---------------------------------------------------
The following information is configured on the pipeline step:

    * Location of the *source object*
    * Location of the *target object*
    * The *value mapping set* to use

Logic Executed by the Pipeline Step
---------------------------------------------------
The pipeline step implements the following logic:

    1. Read the *source object* from the location specified on the pipeline step.
    2. Read the *target object* from the location specified on the pipeline step.
    3. Read the *value mapping set* specified on the pipeline step.
    4. Apply the *value mapping set*.

What "apply the value mapping set" does depends 
on the type of *value mapping set* used. Data Exchange
Framework includes a standard *value mapping set*, but 
developers can implement custom ones.

Logic Executed by the Value Mapping Set
---------------------------------------------------
The standard *value mapping set* iterates the 
*value mappings* assigned to the *value mapping set*.
For each *value mapping*, the following logic runs:

    1. Gets the *source value accessor* assigned to the *value mapping*.
    2. Gets the *value reader* from the *source value accessor*.
    3. Uses the *value reader* to read a value from the *source object*.
    4. If the *source value transformer* is assigned to the *value mapping*, it is used to transform the value that was read from the *source object*.
    5. Gets the *target value accessor* assigned to the *value mapping*.
    6. Gets the *value writer* from the *target value accessor*.
    7. Uses the *value writer* to write the value to the *target object*.
