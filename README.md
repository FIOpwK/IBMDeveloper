# IBMDeveloper
Explore the Java platform, learn object-oriented programming principles, and create a project with IBM


# Getting Started

In this tutorial, you will learn about:

- The function of each of the Java platform's constituent components
- How the Java language is structured
- Navigating the Java API documentation
- Downloading and installing the JDK and the Eclipse IDE
- Setting up your Eclipse development environment
- Understanding the main Eclipse components and how to use them for Java development
- Creating a new Java project in Eclipse
- How the object-oriented paradigm differs from the structured-programming paradigm
- The key characteristics of an object
- The benefits that stem from the defining principles of object-oriented programming (OOP)
## Java platform overview
Java technology is used to develop applications for a wide range of environments, from consumer devices to heterogeneous enterprise systems. In this section, get a high-level view of the Java platform and its components.

## The Java language
Like any programming language, the Java language has its own structure, syntax rules, and programming paradigm. The Java language's programming paradigm is based on the concept of object-oriented programming (OOP), which the language's features support.

The Java language is a C-language derivative, so its syntax rules look much like C's. For example, code blocks are modularized into methods and delimited by braces ({ and }), and variables are declared before they are used.

Structurally, the Java language starts with packages. A package is the Java language's namespace mechanism. Within packages are classes, and within classes are methods, variables, constants, and more. Learn more about the parts of the Java language in the Learn how to create and run Java objects tutorial.

## The Java compiler
When you program for the Java platform, you write source code in .java files and then compile them. The compiler checks your code against the language's syntax rules, then writes out bytecode in .class files. Bytecode is a set of instructions targeted to run on a Java virtual machine (JVM). In adding this level of abstraction, the Java compiler differs from other language compilers, which write out assembly-language instructions suitable for the CPU chipset the program will run on.

## The JVM
At runtime, the JVM reads and interprets .class files and executes the program's instructions on the native hardware platform for which the JVM was written. The JVM interprets the bytecode just as a CPU would interpret assembly-language instructions. The difference is that the JVM is a piece of software written specifically for a particular platform. The JVM is the heart of the Java language's "write-once, run-anywhere" principle. Your code can run on any chipset for which a suitable JVM implementation is available. JVMs are available for major platforms like Linux and Windows, and subsets of the Java language have been implemented in JVMs for mobile phones and hobbyist chips.

## The garbage collector
Rather than forcing you to keep up with memory allocation (or use a third-party library to do so), the Java platform provides memory management out of the box. When your Java application creates an object instance at runtime, the JVM automatically allocates memory space for that object from the heap— a pool of memory set aside for your program to use. The Java garbage collector runs in the background, keeping track of which objects the application no longer needs and reclaiming memory from them. This approach to memory handling is called implicit memory management because it doesn't require you to write any memory-handling code. Garbage collection is one of the essential features of Java platform performance.

## The Java Development Kit
When you download a Java Development Kit (JDK), you get — in addition to the compiler and other tools — a complete class library of prebuilt utilities that help you accomplish most common application-development tasks. The best way to get an idea of the scope of the JDK packages and libraries is to check out the official online Java API documentation — also called the Javadoc. Watch the following quick demo to see how to get around in the Javadoc.

