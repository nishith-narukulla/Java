# Object Oriented Programming Basics

## Class

- class is a user-defined blueprint where objects can be created
- **Modifiers**
    - A class can be public or default
    - but not private or protected
- **ClassName**
    - should start with Capital letter
    - should be only one public class in a single java file
    - should be same as file name if it public class
- **Superclass**
    - a class can have one paarent class
    - usage
    > Class B extends A{ .... }
- **Interfaces**
    - a class can implement more than one interfaces
    - usage
    > Class A implements interface1,interface2 {....}
- **Body**
    - body of the class surrounded by {}

## Object


## Interface

- interface is like a class consisting of methods and variables
- but the methods declared in an interface are by default abstract (only method signature, no body)
- Interfaces specify what a class must do and not how
- So it specifies a set of methods that the class has to implement
- if class implementing interfaces not provides bodies for all the methods mentioned
  in the interface then class must declared as Abstract
- 