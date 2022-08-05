# Using packages

Many HPC systems nowardays have a number of prcompield libraries maintained for users to use with there own codes. These normally fall under four categories:

- Compilers
- Optimised Libraries
- Profilers and debuggers
- Supported user software packages

It is now common for these to be provided via a system of *Modules*.

## Module environment

When any application is installed on a computer it is installed in a specific directory as a selection of files.

When you compile an application with a dependency on another library the library has to be discoverable by the compiler. That is the compiler must be able to see the files it expects in the list of directories it has been told to look in.

This list of directories is defined in various Environment variables called paths. 

- PATH
- LIBRARY_PATH
- LD_LIABRARY_PATH
- INCLUDE
- ...

Managing the setting and uinsetting of these paths by hand can become complex as each peice of software needs a specific combination to be discoverable inorder to work. The Module system offers a frame work for managing these PATH's.

It works by a user (or an automatic tool like spack) defining a module file for each package installed which sets the correct environment variables in order to use the package.

- example module file

This module can then be loaded or unloaded to set the environment parameters for the associated package when it is needed to be used by other applictions.


## Example