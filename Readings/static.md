# static Keyword

## Static Method

- A staic method belongs to class rather than Object
- No nedd to create object to invoke this method
- **Note:** A static method cannot access other non-static variable or method
- Reference: https://www.javatpoint.com/static-keyword-in-java
- Usage
> public static void Name(){
>    ....
> }

> static public void Name(){
>    ....
> }

- Benefits
    - Memory effecient becuase no object creation is needed.
    - main method is always static because of this.

## static variable

- usage
> static int a;

- can be accessible
    - in both static and non-static methods. 