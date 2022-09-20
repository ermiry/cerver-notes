# Programming Languages

**From Wikipedia**
A programming language is any set of rules that converts strings, or graphical program elements, to various kinds of machine code output. A programming language is a notation for writing programs, which are specifications of a computation or algorithm.

**From Britannica**
A programming language expresses a set of detailed instructions for a digital computer. Such instructions can be executed directly when they are in the computer manufacturer-specific numerical form known as machine language, after a simple substitution process when expressed in a corresponding assembly language, or after translation from some “higher-level” language.

## Language Types

### Machine and Assembly Languages
**From Britannica**
Machine and assembly languages are “low-level,” requiring a programmer to manage explicitly all of a computer’s features of data storage and operation. In contrast, high-level languages shield a programmer from worrying about such considerations and provide a notation that is more easily written and read by programmers.

A **machine language** consists of the numeric codes for the operations that a particular computer can execute directly. The codes are strings of binary digits (bits), which are frequently converted both from and to hexadecimal for human viewing and modification. They use bits to represent operations, such as addition, and some to represent operands, or perhaps the location of the next instruction.

**Assembly language** uses short mnemonic codes for instructions and allows the programmer to introduce names for blocks of memory that hold data.

### Algorithmic Languages
**From Britannica**
Algorithmic languages are designed to express mathematical or symbolic computations. They can express algebraic operations in notation similar to mathematics and allow the use of subprograms that package commonly used operations for reuse. They were the first high-level languages.

### Compiled Languages
**From freeCodeCamp**
Compiled languages are converted directly into machine code that the processor can execute. As a result, they tend to be faster and more efficient to execute than interpreted languages. They also give the developer more control over hardware aspects, like memory management and CPU usage. They require a build phase to be executed every time there is a change in the source code.

### Interpreted Languages
**From freeCodeCamp**
Interpreters run through a program line by line and execute each command. Interpreted languages tend to be more flexible, and often offer features like dynamic typing and smaller program size. Also, because interpreters execute the source program code themselves, the code itself is platform independent. The most notable disadvantage is typical execution speed compared to compiled languages. Examples of common interpreted languages are PHP, Ruby, Python, and JavaScript.

## Just-in-Time Compilation
**From freeCodeCamp**
Just-in-time compilation is a method for improving the performance of interpreted programs. During execution the program may be compiled into native code to improve its performance. It is also known as dynamic compilation.

Dynamic compilation has some advantages over static compilation. When running Java or C# applications, the runtime environment can profile the application while it is being run. This allows for more optimized code to be generated. If the behavior of the application changes while it is running, the runtime environment can recompile the code. Some of the disadvantages include startup delays and the overhead of compilation during runtime.

The Java Virtual Machine (JVM) executes bytecode and maintains a count as of how many time a function is executed. If this count exceeds a predefined limit JIT compiles the code into machine language which can directly be executed by the processor (unlike the normal case in which javac compiles the code into bytecode and then Java, the interpreter interprets this bytecode line by line converts it into machine code and executes).

## The C Programming Language

**From The C Programming Language**
C is a general purpose programming language which features economy of expression, modern control flow and data structures, and a rich set of operators. C is not a "very high level" language, and is not specialized to any particular area of application. But its absence of restrictions and its generality make it more convenient and effective for many tasks.

C was originally designed for and implemented on the UNIX operating system on the DEC PDP-11, by Dennis Ritchie. The operating system, the C compiler, and all UNIX applications programs are written in C. The C language is not tied to any particular hardware or system, and it is easy to write programs that will run without change on any machine that supports C.

C provides a variety of data types. The fundamental types are characters, integers and floating point numbers of several sizes. In addition, there is a hierarchy of derived data types created with pointers, arrays, structures, and unions. Expressions are formed from operators and operands; any expression, including an assignment or a function call, can be a statement. Pointers provider for machine-independent address arithmetic.

C provides the fundamental control-flow constructions required for well structured programs: statement grouping, decision making (if-else), selecting one of a set of possible cases (switch), looping with the termination test at the top (while, for) or at the bottom (do), and early loop exit (break).

Functions may return values of basic types, structures, unions or pointers. any function may be called recursively. Local variables are typically "automatic", or created anew with each invocation. function definitions may not be nested but variables may be declared in a block-structured fashion. The functions of a C program may exist in separate source files that are compiled separately. Variables may be internal to a function, external but known only within a single source file, or visible to the entire program.

A pre-processing step perform macro substitution on program text, inclusion of other source files, and conditional compilation.

C provides no operations to deal directly with composite objects such as character strings, sets, lists, or arrays. There are no operations that manipulate an entire array or string, although structures may be copied as a unit.

## Versions of the C programming language
**From The C Programming Language**
The definition of C was the reference manual in the first edition of The C Programming Language. IN 1983, the American national Standards Institute (ANSI) established a committee to provide a modern, comprehensive definition of C. The resulting definition, the ANSI standard, was completed late in 1988. A significant contribution of this standard is the definition of a library that specified functions for accessing the operating system: read and write files, formatted input and output, memory allocation, string manipulation. A collection of standard headers provides uniform access to declarations of functions and data types. Programs that use this library to interact with a host operating system are assured of compatible behavior.

**From developerinsider.co - Vineet Choudhary**
The same standard as ANSI C (C89) was ratified by the International Organization for Standarization (ISO) as ISO/IEC 9899:1990, with only formatting changes.

IN 1995 the ISO published an extension, called Amendment 1, for the ANSI-C standard known as ISO/IEC 9899/AMD1:1995 or nicknamed C95 which included further changes to the languages capabilities:
- Improved multi-byte and wide character support in the standard library.
- Addition of digraphs to the language.
- Specification of standard macros for the alternative specification of operators.

In March 2000, ANSI adopted the ISO/IEC 9899:1999 standard. This is commonly referred to as C99.
- New built-in data types: long long, _Bool, _Complex, and _Imaginary.
- Static array indices, designated initializes, compound literals, variable-length arrays, flexible array members, and restrict keyword.

In 2007, work began on another revision of the C standard, which was officially published in 2011 called C11.
- Type generic macros.
- Anonymous structures.
- Improved Unicode characters support.
- Atomic operations.

## The C Preprocessor
**From The C Programming Language**
C provides certain language facilities by means of a preprocessor, which is conceptually a separate first step in compilation. It is used to include the contents of a file during compilation (via the #include instruction), and to replace a token (created using #define) by a sequence of characters. It can also handle conditional compilation and macros with arguments.

## Pointers
**From Mastering Algorithms in C**
In C, for any type T, we can form a corresponding type for variables that contain addresses in memory where objects of type T reside. One way to look at variables like this is that they actually "point to" the objects. These variables are called **pointers**.

**Pointers** are very important in C; they are a powerful means of building data structures and precisely manipulating memory. However they are also easy to misuse and this can lead to unpredictably buggy software.

**From Mastering Algorithms in C**
A **pointer** is simply a variable that stores the address where a piece of data resides rather than storing the data itself. Pointers contain memory addresses. When a pointer points to nothing at all it is set to the special **NULL** value. Pointers that point to an invalid address are called **dandling pointers**; these can be created when casting arbitrary integers to pointers, adjusting pointers beyond the bounds of an array, or by deallocating storage that storage that one ore more pointers still reference.

## Storage Allocation
**From Mastering Algorithms in C**
when a pointer is declared in C, a certain amount of space is allocated for it just as for other types of variables. Pointers generally occupy one machine word, but their size can vary as result of compiler settings and type specifiers.

Storage for the data is allocated on one of two ways: by declaring a variable for it or by allocating storage dynamically at runtime.

**TO-DO:** Explain stack vs heap memory allocation.

**From Mastering Algorithms in C**
When a variable is declared, its type tells the compiler how much storage to set aside for it as the program runs. Storage for the variable is allocated automatically, but it may not be persistent trough the entire life of the program. **Automatic variables** are those for which storage is allocated and deallocated automatically when entering and leaving a block or function.

**Erick Salas**
In C, when storage is dynamically allocated (usually by calling the **malloc** method), a pointer to the real data in the **heap** is created. It is then the responsibility of the engineer to correctly manage this storage reference as the pointer will remain valid until it is manually deallocated (by calling the **free** method).

The misuse of dynamically allocated storage is a notorious source of memory leaks. A **memory leak** is a block of storage that is allocated but never freed by the program, even when no longer in use; these can enable attackers to gain access to critical information or to enable vulnerabilities and execute malicious code.

**From Mastering Algorithms in C**
**Heap-based Allocation:** The type of memory provided by the C language's functions **malloc** and **realloc**.

**Memory Best Practices**
**Erick Salas**
Memory allocation problems like danging pointers and memory leaks can be reduced by employing consistent approaches to manage storage. For example the storage used by data structures should be self contained; its is the responsibility of the engineer to ensure this by creating methods to initialize and destroy the data structures to expose a reliable interface to the framework's users.

## Aggregates and Pointer Arithmetic
**From Mastering Algorithms in C**
One of the most common uses of pointers in C is referencing aggregate data. **Aggregate data** is data composed of multiple elements grouped together because they are somehow related. C supports two classes of aggregate data: structures and arrays.

## Structures
**From Mastering Algorithms in C**
**Structures** are sequences of usually heterogeneous elements grouped so that they are treated together as a single coherent datatype. Pointers to structures are an important part of building data structures. By linking structures together we can organize them in meaningful ways to help solve real problems.

## Arrays
**From Mastering Algorithms in C**
**Arrays** are sequences of homogeneous elements arranged consecutively in memory. Arrays are closely related to pointers. When an array identifier occurs in an expression, the array is converted transparently into an unmodified pointer that points to the array's first element.

## Generic Pointers
**Erick Salas**
Pointer variables in C have types just like other variables. The main reason for this is so that when we deference a pointer, the compiler knows the type of data being pointed to and can access the data accordingly. Generic pointers can be set to pointers of any type, and vice versa. To make a generic pointer it should be declared using the **void** keyword. They are specially useful when creating data structures as they allow to store and retrieve data of any type.

## Function Pointers
**Function pointers** are pointers that instead of pointing to data, point to executable code or blocks of information need to invoke executable code. They are used to store and manage functions as if they were pieces of data.
