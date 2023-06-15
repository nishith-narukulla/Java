# Strings

- String are objects in java

- usage
    - using new keyword
    > String name = new String("Nishith");
    - this wiil create two objects
      one in heap memory area and
      another one in String constatnt pool
    - object name will refere to object in hep memory(non-pool)

    - using String literal
    > String name = "Nishith";
    - to make java more effecient
    - no new objects created if it exists in string constant pool

## CharSequence Interface

- this interface is used for representing sequence of chars in java
- Classes that are implemented using the CharSequence interface
    - String
        - String represents fixed-length, immutable character sequences

    - StringBuffer
        - it is a peer class of String that provides much of the functionality of strings
        - StringBuffer represents growable and writable character sequences.
        - usage
        > StringBuffer s = new StringBuffer("Nishith");

    - StringBuilder
        - StringBuilder class represents a mutable sequence of characters.
        - usage
        > StringBuilder str = new StringBuilder();

        > str.append("GFG");

    - StringTokenizer
        - class in Java is used to break a string into tokens.

## Immutable Strings in Java

> String name = "Nishith";

> name.concat(" Narukulla");

> System.out.println(name);

- this will print only [Nishith]
- because strings are immutable
- this will create another object with value "Nishith Narukulla"
- name will still refer to "Nishith"
- to make s refer to new object we need to explicitly assign
> name = name.concat(" Narukulla");

> System.out.println(name) // this will print Nishith Narukulla

## String Operations.

- we can create string from an char array
"""
> char[] charArray = {'a', 'b', 'c'};
> String str = new String(charArray); // str --> "abc" 
"""