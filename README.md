# Optimization-of-Delivery-System
optimization of truck and drone delivery system

FICO Xpress Mosel is an analytic orchestration, algebraic modeling, and programming language. Mosel defines a public C interface (Mosel Native Interface) that allows developers to extend the core functionality of the Mosel language according to their needs, such as the definition of data connectors, solver interfaces, or access to system functionality on the Mosel language level. A Mosel program (or model) is a text file that takes the extension .mos, it is compiled into a platform-independent .bim (BInary Model) file that is then loaded by Mosel to be run with some data instance(s).

Mosel source files can be edited with any text editor of your choice, or you can choose to work with the development environment FICO Xpress Workbench that forms part of the Xpress distribution.

This repository contains various extension libraries for the Mosel language, either in the form of Mosel packages (libraries implemented in the Mosel language distributed as platform independent BIM files) or Mosel modules (libraries implemented in C following the conventions of the Mosel Native Interface, also called DSO-dynamic shared objects).

Each subdirectory contains the source of one library, along with building instructions and some test(s).

Furthermore, the moseltest program provides a general testing framework for source Mosel files, C programs or Java programs.

Contents
Modules and packages
Component	Type	Description	Notes
myxprs	DSO	Example of using the Mosel NI matrix handling interface for connecting an LP/MIP solver (Xpress Optimizer)	Requires Xpress Optimizer libraries
myqxprs	DSO	Example of using the library interface of the module mmnl that extends the Mosel NI matrix interface with handling of nonlinearities for connecting an NLP solver (quadratic solver of Xpress Optimizer)	Requires Xpress Optimizer libraries
math	DSO	Additional Maths functions for the Mosel language	Compiled version is included in the Mosel distribution
random	DSO	Alternative random number generators	Compiled version is included in the Mosel distribution
minisat	DSO	Example implementation of a simple interface to a SAT solver	Requires SAT solver libraries
jobqueue	BIM	Managing the remote execution of submodels via mmjobs functionality	-
Mosel testing system
moseltesting General framework for testing Mosel using source Mosel files, C programs or Java programs

Documentation
Mosel documentation:
Mosel Language Reference
Mosel User Guide
Mosel NI Reference
Mosel NI User Guide
Mosel model and program examples: Examples database
Installation
If you do not have any recent installation of FICO Xpress, download the free Xpress Community Edition from Xpress Community Edition download, located on FICO's website. Please note that this download is solely governed under FICO's Xpress Community License, Shrinkwrap License Agreement, FICO Xpress Optimization Suite, FICO Xpress Insight.

Requirements
Mosel modules are C programs, you need a C compiler to generate new DSO.

Contributing
Editing a component
Clone the Mosel Open Source repository.
Edit and test locally.
Submit a pull request.
Adding a new component
Clone the Mosel Open Source repository.
Create a new subdirectory locally complete with makefiles, build instructions and tests.
Submit a pull request.
