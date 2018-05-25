# eos-assemblyscript-preprocessor
Transpiles the @expose decorators.

## Motivation
We do not want our developers to worry about the internal workings of the apply function, or the action_data deserialization. This should be abstracted away, just like it is in the cpp library. As AssemblyScript does not have the required reflection capabilities to do this during runtime, this transpiler is used.

## Design
You simply put @expose("<action>") above the functions you wish to include in the apply function. This preprocessor will than add these functions to the apply function and include piping from the action_data to the actual function arguments.
