# Exception Handling in Java

- usage
> try{
    > ....;
> }

> catch(Exception e){
    > ....;
> }

## Types of Exceptions 
![Img](https://media.geeksforgeeks.org/wp-content/uploads/20220120111809/Group21-660x330.jpg)

## Methods to print the Exception information:
- printStackTrace()
    - prints exception information in the format of Name of the exception: description of the exception
    > e.printTrackTrace();
- toString()
    - prints exception information in the format of Name of the exception: description of the exception.
    > System.out.println(e.toString());
- getMessage()
    - prints only the description of the exception.