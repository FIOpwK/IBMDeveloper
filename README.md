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

## OOP concepts and principles
The Java language is (mostly) object-oriented. This section is an introduction to object-oriented programming (OOP) language concepts, using structured programming as a point of contrast.

## What is an object?
Object-oriented languages follow a different programming pattern from structured programming languages like C and COBOL. The structured-programming paradigm is highly data oriented: You have data structures, and program instructions act on that data. Object-oriented languages such as the Java language combine data and program instructions into objects.

An object is a self-contained entity that contains attributes and behavior, and nothing more. Instead of having a data structure with fields (attributes) and passing that structure around to all of the program logic that acts on it (behavior), in an object-oriented language, data and program logic are combined. This combination can occur at vastly different levels of granularity, from fine-grained objects such as a Number, to coarse-grained objects, such as a FundsTransfer service in a large banking application.

Parent and child objects
A parent object is one that serves as the structural basis for deriving more-complex child objects. A child object looks like its parent but is more specialized. With the object-oriented paradigm, you can reuse the common attributes and behavior of the parent object, adding to its child objects attributes and behavior that differ.

Object communication and coordination
Objects talk to other objects by sending messages (method calls, in Java parlance). Furthermore, in an object-oriented application, program code coordinates the activities among objects to perform tasks within the context of the specific application domain.

## Object summary
A well-written object:

- Has well-defined boundaries
- Performs a finite set of activities
- Knows only about its data and any other objects that it needs to accomplish its activities
In essence, an object is a discrete entity that has only the necessary dependencies on other objects to perform its tasks.

It's time to see what a Java object looks like.

## Example: A person object
My first example is based on a common application-development scenario: an individual being represented by a Person object.

You know from the definition of an object that an object has two primary elements: attributes and behavior. Here's how these elements apply to the Person object.

As a rule of thumb, think of the attributes of an object as nouns and behavior as verbs.

## Attributes (nouns)
What attributes can a person have? Some common ones include:

- Name
- Age
- Height
- Weight
- Eye color
- Gender
You can probably think of more (and you can always add more attributes later), but this list is a good start.

## Behavior (verbs)
An actual person can do all sorts of things, but object behaviors usually relate to application context of some kind. In a business-application context, for instance, you might want to ask your Person object, "What is your body mass index (BMI)?" In response, Person would use the values of its height and weight attributes to calculate the BMI.

More-complex logic can be hidden inside of the Person object, but for now, suppose that Person has the following behavior:

- Calculate BMI
- Print all attributes
- State and string
State is an important concept in OOP. An object's state is represented at any moment in time by the values of its attributes.

In the case of Person, its state is defined by attributes such as name, age, height, and weight. If you wanted to present a list of several of those attributes, you might do so by using a String class, which you'll learn more about later.

Using the concepts of state and string together, you can say to Person, "Tell me all about you by giving me a listing (or String) of your attributes."

## Principles of OOP
If you come from a structured-programming background, the OOP value proposition might not be clear yet. After all, the attributes of a person and any logic to retrieve (and convert) those values can be written in C or COBOL. The benefits of the OOP paradigm become clearer if you understand its defining principles: encapsulation, inheritance, and polymorphism.

## Encapsulation
Recall that an object is above all discrete, or self-contained. This characteristic is the principle of encapsulation at work. Hiding is another term that's sometimes used to express the self-contained, protected nature of objects.

Regardless of terminology, what's important is that the object maintains a boundary between its state and behavior and the outside world. Like objects in the real world, objects used in computer programming have various types of relationships with different categories of objects in the applications that use them.

On the Java platform, you can use access modifiers (which you'll learn about later) to vary the nature of object relationships from public to private. Public access is wide open, whereas private access means the object's attributes are accessible only within the object itself.

The public/private boundary enforces the object-oriented principle of encapsulation. On the Java platform, you can vary the strength of that boundary on an object-by-object basis. Encapsulation is a powerful feature of the Java language.

## Inheritance
In structured programming, it's common to copy a structure, give it a new name, and add or modify the attributes that make the new entity (such as an Account record) different from its original source. Over time, this approach generates a great deal of duplicated code, which can create maintenance issues.

OOP introduces the concept of inheritance, whereby specialized classes — without additional code — can "copy" the attributes and behavior of the source classes that they specialize. If some of those attributes or behaviors need to change, you override them. The only source code you change is the code needed for creating specialized classes. The source object is called the parent, and the new specialization is called the child — terms that you've already been introduced to.

Suppose that you're writing a human-resources application and want to use the Person class as the basis (also called the super class) for a new class called Employee. Being the child of Person, Employee would have all of the attributes of a Person class, along with additional ones, such as:

- Taxpayer identification number
- Employee number
- Salary
- Inheritance makes it easy to create the new Employee class without needing to copy all of the Person code manually.

## Polymorphism
Polymorphism is a harder concept to grasp than encapsulation and inheritance. In essence, polymorphism means that objects that belong to the same branch of a hierarchy, when sent the same message (that is, when told to do the same thing), can manifest that behavior differently.

To understand how polymorphism applies to a business-application context, return to the Person example. Remember telling Person to format its attributes into a String? Polymorphism makes it possible for Person to represent its attributes in various ways depending on the type of Person it is.

Polymorphism, one of the more complex concepts you'll encounter in OOP on the Java platform, is beyond the scope of this introductory course. You'll explore encapsulation and inheritance in more depth in subsequent tutorials.

Not a purely object-oriented language
Two qualities differentiate the Java language from purely object-oriented languages such as Smalltalk. First, the Java language is a mixture of objects and primitive types. Primitive types are the language's most basic data types — the building blocks for data manipulation. Second, with Java, you can write code that exposes the inner workings of one object to any other object that uses it.

The Java language does give you the tools necessary to follow sound OOP principles and produce sound object-oriented code. Because Java is not purely object-oriented, you must exercise discipline in how you write code — the language doesn't force you to do the right thing, so you must do it yourself.

## Overloading methods
When you create two methods with the same name but with different argument lists (that is, different numbers or types of parameters), you have an overloaded method. At runtime, the JRE decides which variation of your overloaded method to call, based on the arguments that were passed to it.

## Overriding methods
When a subclass provides its own implementation of a method that's defined on one of its parent classes, that's called method overriding.

Two or more methods of the same name, but different signatures, are called overloaded methods. When you create a new version of a method in a subclass that is defined in a superclass, it's called method overriding.

# Best coding practices
 Before you continue on to more-advanced topics, this is a good moment to learn a few best coding practices. Read on for some essential pointers that can help you write cleaner, more maintainable Java code.

## Keep classes small
 It's not uncommon (and it's unfortunate) to see classes with 50 or 100 methods and a thousand lines or more of source. Some classes might be that large out of necessity, but most likely they need to be refactored. Refactoring is changing the design of existing code without changing its results. I recommend that you follow this best practice.

In general, a class represents a conceptual entity in your application, and a class's size should reflect only the functionality to do whatever that entity needs to do. Keep your classes tightly focused to do a small number of things and do them well.

## Name methods carefully
A good coding pattern when it comes to method names is the intention-revealing method-names pattern. This pattern is easiest to understand with a simple example. Which of the following method names is easier to decipher at a glance?

- a()
- computeInterest()

The answer should be obvious, yet for some reason, programmers have a tendency to give methods (and variables, for that matter) small, abbreviated names. Certainly, a ridiculously long name can be inconvenient, but a name that conveys what a method does needn't be ridiculously long. Six months after you write a bunch of code, you might not remember what you meant to do with a method called ```compInt()```, but it's obvious that a method called ```computeInterest()```, well, probably computes interest.

## Keep methods small
Small methods are as preferable as small classes, for similar reasons. One idiom I try to follow is to keep the size of a method to one page as I look at it on my screen. This practice makes my application classes more maintainable. 

If a method grows beyond one page, I refactor it. Eclipse has a wonderful set of refactoring tools. Usually, a long method contains subgroups of functionality bunched together. Take this functionality and move it to another method (naming it accordingly) and pass in parameters as needed.

Limit each method to a single job. I've found that a method doing only one thing well doesn't usually take more than about 30 lines of code.

Refactoring and the ability to write test-first code are the most important skills for new programmers to learn. If everybody were good at both, it would revolutionize the industry. If you become good at both, you will ultimately produce cleaner code and more-functional applications than many of your peers

## Use comments
Please, use comments. The people who follow along behind you (or even you, yourself, six months down the road) will thank you. You might have heard the old adage Well-written code is self-documenting, so who needs comments? I'll give you two reasons why I believe this adage is false:

- Most code is not well written.
- Try as we might, our code probably isn't as well written as we'd like to think.

So, comment your code. Period.

## Use a consistent style
Coding style is a matter of personal preference, but I advise you to use standard Java syntax for braces:

```Java
public static void main(String[] args) {
}
```


## Use built-in logging
Before Java 1.4 introduced built-in logging, the canonical way to find out what your program was doing was to make a system call like this one:

```Java
public void someMethod() {
  // Do some stuff...
  // Now tell all about it
  System.out.println("Telling you all about it:");
  // Etc...
}
```
The Java language's built-in logging facility is a better alternative (refer back to "Java language basics" in the "Your first Java class" section). I never use System.out.println() in my code, and I suggest you don't use it either. Another alternative is the commonly used log4j replacement library, part of the Apache umbrella project.


## Conclusion
In this tutorial, you learned about object-oriented programming and familiarized yourself with an IDE that helps you control your development environment.
