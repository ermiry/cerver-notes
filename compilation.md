# Compilation

**From LinkedIn**
The process of converting source code written in any high-level language into machine-level code that is understandable by the computer is known as compilation. The software used for this process is known as a compiler.

In a build process, the compiler checks the source code for syntactic or structural errors, and if everything is perfect, it generates the code object.

The C source code compilation process is a multi-step process, involving pre-processing, code compilation, assembly, and library linking.

**From Scaler**
The compilation process in C is converting an understandable human code into a Machine understandable code and checking the syntax and semantics of the code to determine any syntax errors or warnings present in a C program.

### Pre-Processing
**From Scaler**
Pre-Processing is the first step in the compilation process in C performed using the pre-processor, a program invoked by the system during the compilation.

- **Comments Removal:** Comments in a C Program are used to give a general idea about a particular statement or part of code actually, comments are the part of code that is removed during the compilation process by the pre-processor as they are not of particular use for the machine.
- **Macros Expansion:** Macros are some constant values or expressions defined using the **#define** directives in the C language. A macro call leads to the macro expansion. The pre-processor creates an intermediate file where some pre-written assembly level instructions replace the defined expressions or constants.
- **File Inclusion:** File inclusion in C language is the addition of another file containing some pre-written code into a C source code. It is done using the **#include** directive. The entire contents of the filename are added into the source code, replacing the directive, creating a new intermediate file.
- **Conditional Compilation:** Conditional compilation is running or avoiding a block of code after checking if a macro is defined or not. The preprocessor replaces all the conditional compilation directives with some pre-defined assembly code and passes a newly expanded file to the compiler. Conditional compilation can be performed using any of the **#idef**, **#endif**, **#ifndef**, **#if**, **#else**, **#elif** directives.

### Compiling
**Erick Salas**
In the compiling phase, the intermediate generated sources are converted into **Assembly** instructions.

**From Scaler**
The whole program code is parsed (syntax analysis) by the compiler software in one go, and it can tell about any syntax error or warnings present in the source code.

### Assembling
**From Scaler**
The assembly source code is converted into a machine-understandable code, in binary or hexadecimal form, using and assembler. The assembler is a program that can translate the assembly sources into machine code. It takes basic instructions and converts them into an object code.

### Linking
**From Scaler**
Linking is a process of including the library files into a program. **Library Files** are some predefined files that contain the definition of the functions in the machine language and these files have an extension of **.lib**. It is the final step in compilation to generate an executable file.

## Tools

### GCC
**From GCC**
The GNU Compiler Collection includes front ends for C, C++, Objective-C, FORTRAN, Ada, Go, and D, as well as libraries for these languages. GCC was originally written as the compiler for the GNU operating system.

GCC development is a part of the GNU Project, aiming to improve the compiler used in the GNU system including the GNU/Linux variant. The GCC development effort uses an open development environment and supports many other platforms in order to foster a world-class optimizing compiler, to attract a larger team of developers, to ensure that GCC and the GNU system work on multiple architectures and diverse environments, and to more thoroughly test and extend the features of GCC.

**From Wikipedia**
The GNU Compiler Collection is an optimizing compiler produced by the GNU Project supporting various programming languages, hardware architectures and operating systems. The Free Software Foundation distributes GCC as free software under the GNU General Public License.

### Clang
**From Clang**
The Clang project provides a language front-end and tooling infrastructure for languages in the C language family (C, C++, Objective C/C++, OpenCL, CUDA, and RenderScript) for the LLVM project.

**From LLVM**
The LLVM Project is a collection of modular and reusable compiler and tool-chain technologies. LLVM began as research project project at the University of Illinois, with the goal of providing a modern, SSA-based compilation strategy capable of supporting both static and dynamic compilation of arbitrary programming languages.

Clang is an "LLVM native" C/C++/Objective-C compiler, which aims to deliver amazingly fast compiles, extremely useful error and warning messages and to provide a platform for building great source level tools.

### Make
**From GNU Make**
GNU Make is a tool which controls the generation of executables and other non-source files of a program from the program's source files.

**Erick Salas**
**Makefile** is a special file that can be placed in the source code that tells the **make** utility how to build the program from the existent source code. The **Makfile** contains a list of each required compiled object and how to compute them from the sources.

**From GNU Make**
- Make enables the end user to build and install software packages without knowing the details of how that is done.
- Make figures out automatically which files it needs to update, based on which source files have changed. It also automatically determines the proper order for updating files, in case one non-source file depends on another non-source file. As a result, when changing a few source files and then run **make**, it does not need to recompile all the program.
- Make is not limited to any particular language. For each non-source file in the program, the Makefile specifies the shell commands to compute it. These shell commands can run a compiler to produce an object file, the linker to produce an executable, and so on.
- Make is not limited to building a package, it can also be used to install and removing a package.

A rule in the Makefile tells **make** how to execute a series of commands in order to build a target file from sources files. It also specifies a list of dependencies of the target file.

**Erick Salas**
When writing a large program with multiple source files...

The GNU project has developed a set of conventions and guidelines on how to write Makfiles and structure the compilation process for programs written primarily using the C programming languages. All GNU related packages and many open source projects follow this standard which enable the final users to build them with little effort using the same commands without the need to learn anything different before doing so.
