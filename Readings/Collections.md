# Collections in Java

## it is a Framework :)
- Framework is a collection of  lasses and interfaces which provide a ready-made architecture
- this collection includes useful interfaces like
![Collections](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20201105225856/Collection-Interface-in-Java-with-Examples.png)
 - implementation
 ```java
    Collection<E> objectName = new ArrayList<E>();
 ```
 - E is type of the elements stored in the collection

## List Interface
- This interface is dedicated to the data of the list type in which we can store all the ordered collections of the objects

### ArrayList

- provides us with dyanamic arrays in java
- size grows or shrink automatically by adding and removing elements
- implementation and methods
```java
// implementing arrayList
List<Integer> list = new ArrayList<Integer>();

// Adding elements to the end (element)
list.add(1);
list.add(2);
list.addd(3);

// Adding elements at preferred index (int index, Object)
list.add(0,0);   // 0 1 2 3
list.add(3,4);  // 0 1 2 4 3

// creating an iterator to iterate through list
Iterator<Integer> it = list.iterator();
While(it.hasNext()){
    System.out.println(it.next());
} // 0 1 2 4 3

// removing elements at particular index (int index)
list.remove(3);  // 0 1 2 3
list.remove(0);  // 1 2 3

// removing particular element (Object)
list.remove(Integer.valueOf(2)); // 1 3

// Adding another collection to current list
List<Integer> list2 = new ArrayList<Integer>();
list2.add(4);
list2.add(5);

list.addAll(ist2); // adds at end: 1 2 3 4 5

list.addAll(0,list2); // adds at index 0: 4 5 1 2 3 4 5

// removing another collection from current list (collection)

// getting element at index i (index)
System.out.println(list.get(0)); // 4

// setting element at index with given value (index, value)
list.set(0,0); // 0 5 1 2 3 4 5

// searching for an element (Object)
list.indexOf(5); // returns first occurence: 1
list.lastIndexOf(5); // returns last occurence: 6

// Checking element presence
System.out.println(list.contains(3)); // True

System.out.println(list.contains(6)); // false

System.out.println(list.containsAll(list2)); // true

// other useful methods
list.size(); // returns size
list.clear(); // removes all elements in list
list.isEmpty(); // returns true if empty
Collections.sort(list);
list.sort(null); // sorts the list
```

### LinkedList
- elements are not stored in contiguous locations

### Vector

```java
// same methods as ArrayList
List<Integer> v = new Vector<Integer>();

v.add(2);
v.add(1);
v.add(3);
System.out.println(v);

v.add(0,0);
v.add(4,4);
System.out.println(v);
        
v.remove(4);
v.remove(Integer.valueOf(0));
System.out.println(v);

v.set(0,0);
System.out.println(v);

System.out.println(v.get(0));

System.out.println(v.size());

System.out.println(v.contains(3));

Collections.sort(v);
v.sort(null);
System.out.println(v);

System.out.println(v.isEmpty());
        
System.out.println(v.indexOf(3));
```

### STack

```java
List<Integer> s = new Stack<Integer>();
        
s.add(1);
s.add(2);
s.add(3);
System.out.println(s);

s.add(0,0);
System.out.println(s);

s.remove(0);
System.out.println(s);

s.remove(Integer.valueOf(3));
System.out.println(s);

System.out.println(((Stack<Integer>) s).pop());
System.out.println(s);

s.add(2);
s.add(3);
System.out.println(((Stack<Integer>) s).peek());

System.out.println(((Stack<Integer>) s).empty());
System.out.println(s.isEmpty());

System.out.println(s);
s.set(0,0);
System.out.println(s);

System.out.println(s.get(2));

System.out.println(s.contains(4));

System.out.println(s.indexOf(2));
```

### AbstractList


## Set Interface
- It is an unordered collection of objects in which duplicate values cannot be stored
- 

### HashSet
- an inherent implementation of the hash table data structure or Hashing
- The objects are inserted based on their hash code.
```java
// defining HashMap
HashMap<int, int> hash = new HashMap<>();

// Adding elements to the map
// Also updating elements
hash.put(1,1);
hash.put(2,1);
hash.put(3,1);

// size of the map
sout(hash.size());

// printing elements of map
sout(hash);

// checking key, value existence
hash.containsKey();
hash.containsValue();

// getting value with key
sout(hash.get(1));

// removing element with a key
hash.remove(key);

// iterating through the map
for(Map.Entry<Integer, Integer> map: hash.entrySet()){
    System.out.println(map.getKey() + " --> " + map.getValue());
}

// clears all the mappings
hash.clear();

// cloning to another map
HashMap<Integer, Integer>hash2 = (HashMap<Integer, Integer>) hash.clone();

hash.isEmpty();

hash.keySet(); // [1, 2, 3]

hash.values(); // [2, 1, 1]
```
- **Performance of HashMap**
    - depends on Initial Capacity, Load Factor
**Initial Capacity** 
– It is the capacity of HashMap at the time of its creation (It is the number of buckets a HashMap can hold when the HashMap is instantiated). In java, it is 2^4=16 initially, meaning it can hold 16 key-value pairs.

**Load Factor**
– It is the percent value of the capacity after which the capacity of Hashmap is to be increased (It is the percentage fill of buckets after which Rehashing takes place). In java, it is 0.75f by default, meaning the rehashing takes place after filling 75% of the capacity.

**Threshold**
– It is the product of Load Factor and Initial Capacity. In java, by default, it is (16 * 0.75 = 12). That is, Rehashing takes place after inserting 12 key-value pairs into the HashMap.

**Rehashing**
– It is the process of doubling the capacity of the HashMap after it reaches its Threshold. In java, HashMap continues to rehash(by default) in the following sequence – 2^4, 2^5, 2^6, 2^7, …. so on. 

### LinkedHashSet
- similar to a HashSet
- The difference is that this uses a doubly linked list to store the data and retains the ordering of the elements

### EnumSet
