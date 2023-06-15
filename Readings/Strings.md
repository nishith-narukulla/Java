# String class

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

## String Methods & Operations.

- we can create string from an char array
> char[] charArray = {'a', 'b', 'c'};

> String str = new String(charArray);

> // str --> "abc"

- and we can mention indices to convert specific range of array to string
> String newStr = new String(charArray,0,2); // (array, offset:0, count:2)

> // newStr --> "ab"

> // starting from 0 and 2 characters in array

- .length() method
    - returns length of the string
    > str.length() // 3
- .charAt(int i)
    - returns char at index i
    > str.charAt(1); // b
- .substring(int i, int j)
    - returns substring from index i to end
    > str.substring(1); // bc

    - return substring from index i to j-1
    > str.substring(0,2); // ab
- .concat(String s)
    - it concatenates the string with given string(str)
    - but creates a new object
    - to point reference to the same variable
     > str = str.concat("def")

     > str --> abcdef
- .indexOf(String s, int i)
    - returns the first occurence of string s
    > str.indexOf("d") // index of d: 3

    - returns first occurence of string s from index i
    > str.concat("d"); --> abcdefd

    > str.indexOf("d", 4) // index of d: 6
- .lastIndexOf(String s)
    - returns last occurence of string s
    > str.lastIndexOf("d"); // last index of d: 6
- .equals(String s)
    - returns true if both strings same case sensitive
    > str.equals("abcdefd"); // true

    > str.equals("ABCDEFD"); // false
- .equalsIgnoreCase(String s)
    - returns true if both are same case in-sensitive
    > str.equalsIgnoreCase("ABCDEFD"); // true
- .compareTo(String s)
    - compares two string lexicographically
    - returns:
        - <0 if str comes before s
        - =0 if str and s are same
        - >0 if s comes before str
    > str.compareTo("ABC") // > 0 as ABC comes before str

    > str.compareTo("abcdefd"); // = 0 both are equal

    > str.compareTo("abcdefda") // < 0 as str comes before s
- .compareToIgnoreCase(String s)
    - case in-sensitive
- .toLowerCase()
    - returns lowercase string
    > str.lowercase(); // abcdefd
- .toUpperCase()
    - returns upper case string
    > str.toUpperCase(); // ABCDEFD
- .trim()
    - removes whitespaces at both ends
- .replace(char oldChar, char newChar)
    - replaces all occurences of oldChar by newChar


# StringBuffer class

- StringBuffer class represents sequence of mutable characters
- usage
> StringBuffer str = new StringBuffer("Nishith");

## StringBuffer Methods

- .append(String s)
    - appends s to the last
    > str.append(" Narukulla"); // Nishith Narukulla
- .insert(int i, object)
    - insert given object at given index
    > str.insert(7, " Narukulla"); // Nishith Narukulla

    > str.insert(0, "R"); // RNishith
- .delete(int i, int j)
    - deletes range of chars from i to j
    > str.delete(3,6) // Nish (3,4,5 will be removed)
- .reverse()
    - reverses the string
- .replace(int i, int j, String str)
     - replaces with given string
- .length()
- .capacity()
- .charAt()	
- .deleteCharAt()

## StringTokenizer class

- this class is used to split the string by giving a delimiter(seperator)
- [Reference](https://www.geeksforgeeks.org/stringtokenizer-class-in-java/)

- usage:1
> StringTokenizer str = new StringTokenizer("Hello Nishith", " ");

> while(StringTokenizer.hasMoreTokens()){

>   System.out.println(str.nextToken());

> }

> // Hello Nishith

- usage:2
> StringTokenizer str = new StringTokenizer("Hello Nishith", " ", true);

> while(str.hasMoreTokens()){

>   System.out.println(str.nextToken());

> } // "Hello", " ", "Nishith"

- usage:3
> StringTokenizer str = new StringTokenizer("2*3+456-434=643+5353*g4t", "*=+-");

> while(str.hasMoreTokens()){

>   System.out.println(str.nextToken());

> } // 2 3 456 434 643 5353 g4t