# GCC - the Essentials

## What is the GCC?

GCC stands for “GNU Compiler Collection”. GCC is an integrated distribution of compilers for several major programming languages. These languages currently include C, C++,
Objective-C, Objective-C++, Fortran, Ada, D, Go, and BRIG (HSAIL).  

> *When we talk about compiling one of those languages, we might refer to that compiler by its own name, or as GCC. Either is correct.*

The language-independent component of GCC includes the majority of the optimizers, as well as the *“back ends”* that generate machine code for various processors.  The part of a compiler that is specific to a particular language is called the *“front end”*. For example the C front-end is called CC, the C++ compiler is G++, the Ada compiler is GNAT, and so on.  

Historically, compilers for many languages, including C++ and Fortran, have been implemented as “preprocessors” which emit another high level language such as C. None of
the compilers included in GCC are implemented this way; they all generate machine code directly.

#### C Standards supported by GCC

GCC supports all C standards starting ANSI C Standard in 1990 upto more recent C2X standard, which has mostly experimental support. GCC also provides some extensions to the C language - GNU Extensions that, on rare occasions conflict with the C standard. Use of the ‘-std’ options listed below disables these extensions where they conflict with the C standard version selected.

|  C Standard |  Language option  | GNU Extension |
|:-----------:|:-----------------:|:-------------:|
| ANSI or C90 | -ansi or -std=c90 |  -std=gnu90   |
|     C99     |      -std=c99     |  -std=gnu99   |
|     C11     |      -std=c11     |  -std=gnu03   |
|     C17     |      -std=c17     |  -std=gnu17   |
|     C2X     |      -std=c2x     |  -std=gnu2x   |

> *The default, if no C language dialect options are given, is ‘-std=gnu17’.*

#### C++ Standards supported by GCC

GCC supports the original ISO C++ standard published in 1998, and the 2011, 2014, 2017 and mostly 2020 revisions. By default, GCC also provides some additional extensions to the C++ language that on rare occasions conflict with the C++ standard. Use of the ‘-std’ options listed below disables these extensions where they they conflict with the C++ standard version selected.

|        C++ Standard       |   Language option   | GNU Extension |
|:-------------------------:|:-------------------:|---------------|
| ISO C++ Standard or C++98 | -ansi or -std=c++98 | -std=gnu++98  |
|           C++03           |      -std=c++03     | -std=gnu++03  |
|           C++11           |      -std=c++11     | -std=gnu++11  |
|           C++14           |      -std=c++14     | -std=gnu++14  |
|           C++17           |      -std=c++17     | -std=gnu++17  |
|           C++20           |      -std=c++20     | -std=gnu++20  |

> *The default, if no C language dialect options are given, is ‘-std=gnu++17’.*


 ## Compiling with GCC

After you edit your source code with a text-editor, the next step is to to compile your program using GCC.  When you invoke GCC, it normally does preprocessing, compilation, assembly and linking.


```Shell
g++ -std=<std> -o <executable> <src1.cpp> [src2.cpp ...]              # to compile witha specific version of C++
```

In order to debug an executable, it must be compiled with –g flag to save the symbol table. The symbol table contains the list of memory addresses corresponding to the variables and various machine instructions.

```Shell
gcc -Wall –g -o <executable_name>  <source files>
gcc –Wall –Og –o <executable_name> <source files>
gcc –Wall –std=C++17 –Og –o <executable_name> <source files>
```

Run the program as follows:

```Shell
./<executable>
```

## A Summary of GCC Command Options

* Overall Options
* C language Options
* C++ Language Options
* Diagnostic Message Formating Options
* Warning Options
* Static Analyzer Options
* Debugging Options
* Optimization Options
* Program Instrumentation Options
* Pre-processor Options
* Assembler Options
* Linker Options
* Directory Options
* Code Generation Options
* Others
 * Developer Options
 * Machine Dependent Options
## Common File Formats
## Difference in behaviour - cc vs g++

https://www3.ntu.edu.sg/home/ehchua/programming/cpp/gcc_make.html  
https://www3.ntu.edu.sg/home/ehchua/programming/index.html  
http://web.cs.ucla.edu/classes/fall14/cs143/project/cpp/gcc-intro.html  
https://courses.cs.washington.edu/courses/cse451/99wi/Section/gccintro.html   
https://www.geeksforgeeks.org/compiling-with-g-plus-plus/  
https://riptutorial.com/cplusplus/example/1334/compiling-with-gcc  
https://riptutorial.com/gcc  
https://web.stanford.edu/class/cs107/resources/gcc  