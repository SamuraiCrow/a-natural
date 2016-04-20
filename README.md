# A Natural

The goal of this project is to produce an AROS-specific framework for statically compiled languages without a garbage-collection requirement.  It will be modelled after the C++14 STL and other frameworks built on top of it.  Among the chief goals is to implement the entire LLVM compiler framework with reentrant, thread-safe, AROS shared libraries.

One noteworthy deviation from the C++14 STL is that it won't require support for run-time type information (RTTI) but instead will resolve the type information at compile time by default for better performance.  When LLVM first adopted its template-based solution over the default C++ RTTI solution, it enjoyed an 11% speed increase when compiling its own source code.

Another deviation is that all AROS supported primitive data types will have wrapper code for all functions so that functional programming using pass-by-reference will be possible with minimal overhead.

See the Wiki for more specific information.
