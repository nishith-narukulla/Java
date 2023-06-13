# Basics

## JVM(Java Virtual Machine)

- Reference: https://www.geeksforgeeks.org/jvm-works-jvm-architecture/
- JVM is a part of JRE(Java Runtime Environment)
- when we compile .java file
  .class(with byte-code will be generated)
- this .class file go through different stages
![Flow](https://media.geeksforgeeks.org/wp-content/uploads/jvm-3.jpg)

- **Method Area**
  - Only one method Area per JVM
  - it is a dshared resource
  - contains class level info(class names, parent classes, mrthods, variables)
  - from java8 static variables are now storing in Heap Memory

- **Heap Area**
  - One per JVM
  - shared resource
  - sores info about Objects

- **Stack Area**
  - a run-time stack
    which consists of method calls & its variables
  - once the thread is completed this stack will be destroyed

- **PC Registers**
  - stores adress of executing instruction
  - every thread has its own register

- **Native method stacks**
  - stores native method info
  - every thread has its own stack

------------------------END of JVM Basics----------------------

- class name should match with File name
- we can create multiple classes in a single file but
  there should be only one public class in a file.
- usage
> public class Main{
  .....
}

> class AnotherClass{
  ....
}

## Datatypes

- **primitive datatypes**
  - Primitive data are only single values and have no special capabilities.
  - boolean, char, int, short, byte, long, float, and double

- **Non-primitive datatypes** or **Reference data types**
  - Reference Data Types will contain a memory address of variable values
  reference types won’t store the variable value directly in memory
  - String, Array, classes, interfaces etc

- **Difference between Primitive & Non-primitive**
  - Primitive
  > int a = 10;
  > int b;
  > b = a;
  > b = 11;
  > System.out.println("a: " + a); // 10
  > System.out.println("b: " + b); // 11
  > a & b both points to different locations

  - Non-primitive
  > int[] a = {10,20,30,40,50};
  > int[] b;
  > b = a;
  > b[1] = 200;
  > System.out.println("a[1]: " + a[1]); // 200
  > System.out.println("b[1]: " + b[1]); // 200
  > a & b points to the same Heap memory location
  > Here the entire reference of a is copied to b

## IdentifierS

- Identifier is nothing but name of class, method, variable
- Java identifiers are case sensitive
- reserved keywords cant be used as identifiers

## Types of VAriables

- **Local Variables**
  - variables defined in a specific block or function
  - they are created when execution entered the block and destroyed when execution completed or
    when function call return
  - scope of these variables exists only within the block in which the variables are declared

- **Instance Variables**
  - these are non-static variables
  - defined in a class outside of any methods, blocks, constructors
  - these are created when we create a object
  - we initialize instance variables using constructors
  - creates as many variables as we keep on creating objects
  - changes made using one onject will not reflect other objects
  - destroyed when the object is destroyed

- **Static Variables**
  - These variables are also created inside class and outside of any method,constructor and blocks
  - the difference is that these are declared with key word static
  - and no need to create object for accessing them.
  - we can using class name
  - if we access with any object compiler give us warnings but dont stop the flow
  - object name automatically replaces with class name
  - created only once irrespective of how many objects created
  - good for memory management
  - if changed once it will change for whole class(common for all objects)
  - destroyed when program stops