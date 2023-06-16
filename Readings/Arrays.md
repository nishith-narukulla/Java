# Arrays

- Arrays are stored in contiguous memory
- An array can contain primitives (int, char, etc.) and object (or non-primitive) references
### declaration
    > type var_name[];

    > type[] var_name;
- array references to objects of MyClass
    > MyClass arr[];
- array of objects
    > Objects[] arr;
- array of collections
    > Collection[] arr;

### allocating size to an array
    > type arr[];

    > arr = new type[size]
    or
    > type arr[] = new type[size]

    > int arr[] = new int[20]

    - The elements in the array allocated by new will automatically be initialized to zero (for numeric types)
      false (for boolean)
      or null (for reference types)
### assigning elements
> int[] arr = {1,2,3,4,5};

> arr[0] = 1;

### Accessing elements using loops

- for loop:

> for (int i=0; i < arr.length; i++){

>     System.out.println(arr[i]);

> } // 1 2 3 4 5

for-each loop:

> for (int value: arr){

>   System.out.println(value);

> } // 1 2 3 4 5

## Array Class

- this class provides various methods to work on arrays easily

### Methods 

> int arr[] = {1,2,35,7,4,3,69};

- binarySearch()
    - searches for the specified element using BS Algo
    > Arrays.binarySearch(35); // 2
- binarySearch(array, fromIndex, toIndex, key, Comparator)
    - Searches a range of the specified array for the specified object
    > Arrays.binarySearch(arr, 2, 5, 4); // 4  (fromIndex:2 toIndex:5 Object:4)
- compare(array 1, array 2)
    - Compares two arrays lexicographically
- copyOf(originalArray, newLength)
    - copies the specified array with new length
    > newArray = Arrays.copyOf(arr, 10)

    > System.out.println(Arrays.toString(newArray)); // 1 2 35 7 4 3 69 0 0 0
- copyOfRange(originalArray, fromIndex, endIndex)	
    - Copies the specified range of the specified array into a new Arrays.
    > System.out.println(Arrays.copyOfRange(arr, 2,6)); // 35 7 4 3
- equals(array1, array2)	
    - checks if the two arrays equal
    > System.out.println(Arrays.equals(arr,newArray)); false
- fill(originalArray, fillValue)	
    - fills entire array with given value
    > System.out.println(Arrays.toString(Arrays.fill(arr, 10))); // 10 10 10 10 10 10 10 10 10 10
- mismatch(array1, array2)
    - Finds and returns the index of the first unmatched element between the two specified arrays.
    > System.out.println(Arrays.mismatch(arr, newArray)); 7
- sort(originalArray)	
    - sorts array in ascending order
    > Arrays.sort(arr); // 1 2 3 4 7 35 69
- sort(originalArray, fromIndex, endIndex)
    - sorts the given range of array
    > Arrays.sort(arr, 2, 4); // 1 2 7 35 4 3
- toString(originalArray)
    - returns string repr of array elements
    > System.out.println(Arrays.toString(arr)); // [1,2,35,7,4,3,69]