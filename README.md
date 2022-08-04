# CompareSimple


## Overview

`CompareSimple` offers a couple of methods designed to compare functions, operators, scripts and files. It is also able to deal with SALTed or Linked files.


## Methods

There are just two main functions:


### The function `Match`

`Match` takes the names of functions or operators or scripts and compares the code. Note that taking the source code with `⎕CR` or `⎕SRC` and then `≡` them is not always going to work: white spaces as well as formatting problems might result in a 0 when the source code is in fact identical. `Match` deals with these problems properly.


### The function `These`

`These` accepts a variety of arguments listed underneath. According to its arguments it tries to figure out what your intention is and carries out the appropriate action.

Note that whenever the word "function" is used here it can also be a defined operator.


#### Script / script

Compare the two scripts. Note that you can specify name(s) as well as reference(s).


#### Script / name of a code file

A code file may have the extension `.aplf`, `.aplo`, `.apln`, `.aplc`, `.apli` or `.dyalog`.

Compare the workspace script with the file.


#### Script

This syntax requires "Script" to be managed either by SALT or by acre.

    If it is managed by acre then a dialog pops up with the number of all versions saved by acre.
    If it is managed by SALT the workspace script is compared with its SALTed source file. 

Note however that for acre this requires the script in question to be a member of an opened acre project at the time the comparison is carried out.


#### Name of a native file / name of a native file

Compare the two files.


#### Function name / function name

Compare two functions in the workspace.


#### Function name / name of a native file

Compare the function in the workspace with the contents of that file.


#### Function name / name of an acre component file

Compare the function in the workspace with the acre component file.


#### Function name

If it is managed by acre then a dialog pops up with the number of all versions saved by acre.

Note that the function in question must be a member of an opened acre project at the time the comparison is carried out.


#### Namespace / namespace

Note that this works only with named namespaces, although the arguments might be either references or names pointing to the two namespaces. 