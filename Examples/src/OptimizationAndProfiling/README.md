#This directory contains a series of examples of optimization and profiling. #

* `make esempioExtAss`: produces an example of use of the extendedAssert
     facility provided in the directory Utilities/ (to use it you have to go in that directory 
     and follow the instruction to install the code, if you have not already done it). The programs `esempioExtAss_debug` and `esempioExtAss_release` are generated one with the assertions
     activated and the other not. The file `Rational.dat` is read and contains a list of rationals in the form numerator denominator.
     It may be modified to assess the activation of the assertions (try a zero denominator).

* `make optimize` shows the effect of different optimization level on the CPU time to solve a simple fem program. In the file dati you should write the number of elements you want. Suggested: 300.

* `make debug`. Produces two executable esempio0_debug and
     esempio1_debug. The latter contains an error. You should try to
     use the debugger use ulimit -c unlimited to do static debugging

* `make leak`. An example of use of valgrind to find a memory leak. You should have valgrind installed


* `make profile`. An example of use of `gprof` profiler. The --annotated-source option is not working with the current version of `g++`
	 on my computer. Try it on yours.

* `make massif`. An example of use of `massif` tool of `valgrind`  to analyze memory usage.

* `make aliasing`: a code that may produce wrong results because of aliasing

* `make coverage` : use of `gcov` to to the coverage of a program. It produces a lot
     of files, but you can clean it up using make clean
     
* `namemangling,cpp` does not create any executable. is only to test namemangling. You should do `g++ -c namemangling.cpp`
    and run `nm namemangling.o` or `nm --demangle namemangling.o` to see the difference.

`rational.[h|c]pp` and `GetPot` are only support utilities used in some of the previous examples. 