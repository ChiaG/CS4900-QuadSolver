# CS4900 Quadratic Solver

Mitchell Hobner, Dustin Robbins, Shahbaaz Singh

## IMPORTANT
Users will need to install the The GNU Multiple Precision Arithmetic Library to use this program.

You can learn about GMP and its functions here: https://gmplib.org/manual/

You can download GMP here: https://gmplib.org/#DOWNLOAD
... and find directions on how to install it here: https://gmplib.org/manual/Installing-GMP.html#Installing-GMP

Note that to use GMP you must link the -lgmp and -lm libraries. This is done in our makefiles by default.

## Installation
Aside from the installation of GMP as mentioned above, no installation is needed to run this program. Simply enter src/main/ and enter `make run` on the command line.

## Abstract
This program's purpose is to, given three floating-point numbers a, b, and c, return the "roots" of a quadratic equation with those coefficients (form of "ax^2 + b x + c"). To run it, simply enter /src/main/ and enter `make test` in the command line. A user will be prompted to enter a, b, and c in that order, and will then be given the discriminant of that function (equivalent to "b^2 - 4ac"), and the roots of that function (equivalent to (-b +|- sqrt(b^2 - 4ac)\2a) if there are any.

For more information on the quadratic formula and associated terms, here's the Wikipedia article on the topic: https://en.wikipedia.org/wiki/Quadratic_formula

## Directory Structure
* doc/
  * Documentation on how we managed the project (source control, coding standard, etc) as well as some general information on IEEE floating-point numbers
* spikes/
  * gmp-basics/
    * Tests basic functionality of GMP, really just preactice using the mpf_t data type and compiling a program using the library
  * sprt_compare/
    * Compares GMP's result for the square root of 2 against the result obtained from Google's caluculator, just to see the accuracy of the mpf_t data type.
  * sscanf_test/
    * This tested whether it was possible for us to us sscanf to screen for NaN and 0 inputs
* src/
  * main/
    * Our program's main method and an accompanying makefile
  * modules/
    * Our source modules containing functions for input validation (runtimeLoad) and finding the roots of a quadratic equation with the given coefficients, along with header files for both modules
  * tests/
    * This directory has folders each containing a test driver for each source module and a makefile to manage said test, as well as a logs/ directory that contains text files for those tests to print results to
