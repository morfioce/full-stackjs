# Modules

The module system is based on the `require` function which is used to load anything from:
  - built-in modules
  - downloaded libraries
  - files that are part of your own program.

* When require is called, Node has to resolve the given string to an actual file.

Pathnames that start with `"/"`, `"./"`, or `"../"` are resolved relative to the current module’s path, where:

* `"./"` stands for the current directory

* `"../"` for one directory up

* `"/"` for the root of the file system.

* So if you ask for `"./world/world"` from the file `/home/marijn/elife/run.js`.
* Node will try to load the file `/home/marijn/elife/world/world.js`.

The `.js` extension may be omitted.

When a string that does not look like a relative or absolute path is given to require

It is assumed to refer to either a built-in module or a module installed in a node_modules directory.

For example:

* `require("fs")` will give you Node’s built-in file system module.
* `require("elife")` will try to load the library found in `node_modules/elife/`.

## Exercises

Write a javascript module that exports a function "sum" that return the sum of it's arguments

require and call "sum" function and print it's result.
