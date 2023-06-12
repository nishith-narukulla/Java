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