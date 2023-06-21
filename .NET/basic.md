
### Garbage collection
a process that use to collect and remove programs that they are no longer using, helps increase the memory space and that the garbage collector works like a memory manager

# CLR 
Common Language Runtime and it is an Execution Environment. It works as a layer between Operating Systems and the applications written in .NET languages that conforms to the Common Language Specification (CLS). 
# The main function of CLR is to convert the Managed Code into native code and then execute the program.

### Name some CLR services? 
Assembly Resolver
Assembly Loader
Type Checker
COM marshalled
Debug Manager
Thread Support
IL to Native compiler
Exception Manager
Garbage Collector

### What is CoreCLR?  
The execution engine and runtime environment for .NET Core applications

CoreCLR is the .NET execution engine in .NET Core, performing functions such as garbage collection and compilation to machine code.


# Here are some key features and aspects of CoreCLR:
Just-in-time (JIT) compilation: CoreCLR includes a just-in-time compiler that translates intermediate language (IL) code into machine code at runtime. This compilation process improves performance by optimizing code execution for the target platform.

Garbage collection: CoreCLR includes a garbage collector that manages memory allocation and deallocation for .NET Core applications. It automatically frees up memory occupied by objects that are no longer in use, ensuring efficient memory management.

Cross-platform support: CoreCLR is designed to be cross-platform, enabling .NET Core applications to run on Windows, macOS, and Linux. It provides a consistent runtime environment across different operating systems, allowing developers to build and deploy applications with ease.

Security and sandboxing: CoreCLR incorporates security features to ensure safe execution of .NET Core applications. It provides mechanisms for code access security, sandboxing, and isolation to protect against malicious or unauthorized actions.

Performance optimizations: CoreCLR includes various performance optimizations, such as just-in-time compilation, which improves the execution speed of managed code. It also supports features like background just-in-time compilation and tiered compilation to further enhance performance.

Interoperability: CoreCLR enables interoperability between managed .NET code and native code. It provides mechanisms to call native code from managed code and vice versa, allowing developers to leverage existing native libraries or take advantage of low-level system functionality.

CoreCLR is a critical component of the .NET Core runtime stack and plays a crucial role in executing and managing .NET Core applications. It provides a runtime environment that enables developers to write and run cross-platform, high-performance applications using the .NET Core framework.

# CTS (Common Type System)


### Name two data types the CTS supports.
* Reference types: that store memory address references 
* Value types: that include standard primitive types (also known as built-in value types) 

# MSIL
 .NET codes convert to MSIL before the CLR interprets it

# Explain what SDK is in .NET
SDK is a collection of libraries and tools. Developers use SDK to create .NET applications and libraries. 

# .NET Standard
Use .NET Standard to create a shared library that they can use again with any .NET platform. 
.NET Standard is a specification that determines what the base class library needs to implement for easy code sharing. The code is shared between applications running on different platforms.


# JIT compilers
Before a computer can execute the source code, special programs called compilers must rewrite it into machine instructions, also known as object code. This process (commonly referred to simply as “compilation”) can be done explicitly or implicitly.

Implicit compilation is a two-step process:

The first step is converting the source code to intermediate language (IL) by a language-specific compiler.
The second step is converting the IL to machine instructions. The main difference with the explicit compilers is that only executed fragments of IL code are compiled into machine instructions, at runtime. The .NET framework calls this compiler the JIT (Just-In-Time) compiler.

# State Management in ASP.NET
### Server-Side
* Session
* Application
* Cache
### Client-Side
* Cookies 
* Viewstate
* Control state
* Query String
* Hidden Field 