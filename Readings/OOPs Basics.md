# Object Oriented Programming Basics

## Class

- class is a user-defined blueprint where objects can be created
- a class represents set of methods that are common for all objects
- Class does not occupy memory
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
- **Constructor**
    - initializes object with given fields
    - constructor method name should match with class name
    > public myClass(String nmae, int age){

         this.name = name;

         this.age = age;

     } 

## Object
    - ways of creating object
        - new key word
        > Test obj = new Test();

        - Using Class.forName
        > Test obj = (Test)Class.forName("java.com.p1.Test").newInstance();

        - Using clone()
        > Test obj2 = (Test)obj.clone();

## Interface

- interface is like a class consisting of methods and variables
- but the methods declared in an interface are by default abstract (only method signature, no body)
- Interfaces specify what a class must do and not how
- So it specifies a set of methods that the class has to implement
- if class implementing interfaces not provides bodies for all the methods mentioned
  in the interface then class must declared as Abstract

## Four Pillars of OOPs

![OOPs](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20190717114649/Object-Oriented-Programming-Concepts.jpg)

### Abstraction

- it is the property by which only esential properties are made visible to user.
- abstraction is achieved by interfaces(100%) and abstract classes.
- abstract method only contains method declaration not implementation
> abstract class myClass{

>   abstract void add();

>   abstract int mul();

> }

### Encapsulation

- wrapping up of data under a single unit
- Technically in encapsulation the variables or the data in a class is hidden from any other class
- and these data can be accessed using member function of that class
- basically encapsulation is done by declaring variables as private
- and we can write public setters and getters to access that variables

### Inheritance

- one class is allowed to inherit features of another class
- this ensures code re-usability
> class B extends A{ .... }

### Polymorphism

- The ability to appear in many forms is called polymorphism.
- > void add(int x, int y){
    System.out.println(x+y);
}

> void add(int x, int y, int z){
    System.out.println(x+y+z);
}

> add(2,3); // 5

> add(2,3,4); // 9

- Overloading can be done in 3 ways
    - Overloading is about the same function have different signatures.
    - compiler time polymorphism
    - changing number of parameters
    - changing data types
    - changing the order of paraameters
    - Objects of a class can also be initialized in different ways using the constructors

- overriding
    - Overriding is about the same function, same signature but different classes connected through inheritance.
    - run time polymorphism

![image](http://media.geeksforgeeks.org/wp-content/uploads/OverridingVsOverloading.png)
