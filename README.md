# collections-framework
# ArrayList
Java ArrayList class uses a dynamic array for storing the elements. It is like an array, but there is no size limit. We can add or remove elements anytime. 
So, it is much more flexible than the traditional array. It is found in the java.util package. It is like the Vector in C++.

The ArrayList in Java can have the duplicate elements also. It implements the List interface so we can use all the methods of the List interface here. 
The ArrayList maintains the insertion order internally.

It inherits the AbstractList class and implements List interface.

**The important points about the Java ArrayList class are:**

* Java ArrayList class can contain duplicate elements.
* Java ArrayList class maintains insertion order.
* Java ArrayList class is non synchronized.
* Java ArrayList allows random access because the array works on an index basis.
* In ArrayList, manipulation is a little bit slower than the LinkedList in Java because a lot of shifting needs to occur if any element is removed from the array list.
* We can not create an array list of the primitive types, such as int, float, char, etc. It is required to use the required wrapper class in such cases.
* Java ArrayList gets initialized by the size. The size is dynamic in the array list, which varies according to the elements getting added or removed from the list.

## Java LinkedList class
Java LinkedList class uses a doubly linked list to store the elements. It provides a linked-list data structure.
It inherits the AbstractList class and implements List and Deque interfaces.

**The important points about Java LinkedList are:**
* Java LinkedList class can contain duplicate elements.
* Java LinkedList class maintains insertion order.
* Java LinkedList class is non synchronized.
* In Java LinkedList class, manipulation is fast because no shifting needs to occur.
* Java LinkedList class can be used as a list, stack or queue.

Doubly Linked List
In the case of a doubly linked list, we can add or remove elements from both sides.

## Difference between ArrayList and LinkedList
https://www.javatpoint.com/difference-between-arraylist-and-linkedlist

## Java List
List in Java provides the facility to maintain the ordered collection. 
It contains the index-based methods to insert, update, delete and search the elements. 
It can have the duplicate elements also. We can also store the null elements in the list.

The List interface is found in the java.util package and inherits the Collection interface. 
It is a factory of ListIterator interface. Through the ListIterator, we can iterate the list in forward and backward directions. 
The implementation classes of List interface are ArrayList, LinkedList, Stack and Vector. 
The ArrayList and LinkedList are widely used in Java programming. The Vector class is deprecated since Java 5.

## Why not to use vector in your class - It is deprecated after java 1.5
https://javaconceptoftheday.com/not-use-vector-class-code/

## Java HashSet

Java HashSet class hierarchy
Java HashSet class is used to create a collection that uses a hash table for storage. It inherits the AbstractSet class and implements Set interface.

The important points about Java HashSet class are:

* HashSet stores the elements by using a mechanism called hashing.
* HashSet contains unique elements only.
* HashSet allows null value.
* HashSet class is non synchronized.
* HashSet doesn't maintain the insertion order. Here, elements are inserted on the basis of their hashcode.
* HashSet is the best approach for search operations.
* The initial default capacity of HashSet is 16, and the load factor is 0.75.
* Difference between List and Set
* A list can contain duplicate elements whereas Set contains unique elements only.


## Java LinkedHashSet Class
Java HashSet class hierarchy
Java LinkedHashSet class is a Hashtable and Linked list implementation of the Set interface. It inherits the HashSet class and implements the Set interface.

**The important points about the Java LinkedHashSet class are:**

* Java LinkedHashSet class contains unique elements only like HashSet.
* Java LinkedHashSet class provides all optional set operations and permits null elements.
* Java LinkedHashSet class is non-synchronized.
* Java LinkedHashSet class maintains insertion order.

**_Note: Keeping the insertion order in the LinkedHashset has some additional costs, both in terms of extra memory and extra CPU cycles. 
Therefore, if it is not required to maintain the insertion order, go for the lighter-weight HashMap or the HashSet instead._**

Difference between Hashset and LinkedHashset - Linked hashset maintains insertion order
https://www.javatpoint.com/hashset-vs-linkedhashset-in-java

## Java TreeSet class
TreeSet class hierarchy
Java TreeSet class implements the Set interface that uses a tree for storage. It inherits AbstractSet class and implements the NavigableSet interface. The objects of the TreeSet class are stored in ascending order.

**The important points about the Java TreeSet class are:**

* Java TreeSet class contains unique elements only like HashSet.
* Java TreeSet class access and retrieval times are quiet fast.
* Java TreeSet class doesn't allow null element.
* Java TreeSet class is non synchronized.
* Java TreeSet class maintains ascending order.
* Java TreeSet class contains unique elements only like HashSet.
* Java TreeSet class access and retrieval times are quite fast.
* Java TreeSet class doesn't allow null elements.
* Java TreeSet class is non-synchronized.
* Java TreeSet class maintains ascending order.
* The TreeSet can only allow those generic types that are comparable. For example The Comparable interface is being implemented by the StringBuffer class.

**Internal Working of The TreeSet Class**
TreeSet is being implemented using a binary search tree, which is self-balancing just like a Red-Black Tree. 
Therefore, operations such as a search, remove, and add consume O(log(N)) time. 
The reason behind this is there in the self-balancing tree. It is there to ensure that the tree height never exceeds O(log(N)) for all of the mentioned operations.
Therefore, it is one of the efficient data structures in order to keep the large data that is sorted and also to do operations on it.

**Synchronization of The TreeSet Class**
As already mentioned above, the TreeSet class is not synchronized. 
It means if more than one thread concurrently accesses a tree set, and one of the accessing threads modify it, then the synchronization must be done manually. 
It is usually done by doing some object synchronization that encapsulates the set. 
However, in the case where no such object is found, then the set must be wrapped with the help of the Collections.synchronizedSet() method. 
It is advised to use the method during creation time in order to avoid the unsynchronized access of the set. The following code snippet shows the same.

## Java Queue Interface
The interface Queue is available in the java.util package and does extend the Collection interface. 
It is used to keep the elements that are processed in the First In First Out (FIFO) manner. 
It is an ordered list of objects, where insertion of elements occurs at the end of the list, and removal of elements occur at the beginning of the list.

Being an interface, the queue requires, for the declaration, a concrete class, and the most common classes are the LinkedList and PriorityQueue in Java. 
Implementations done by these classes are not thread safe. 
If it is required to have a thread safe implementation, PriorityBlockingQueue is an available option.

**Features of a Queue**
The following are some important features of a queue.

* As discussed earlier, FIFO concept is used for insertion and deletion of elements from a queue.
* The Java Queue provides support for all of the methods of the Collection interface including deletion, insertion, etc.
* PriorityQueue, ArrayBlockingQueue and LinkedList are the implementations that are used most frequently.
* The NullPointerException is raised, if any null operation is done on the BlockingQueues.
* Those Queues that are present in the util package are known as Unbounded Queues.
* Those Queues that are present in the util.concurrent package are known as bounded Queues.
* All Queues barring the Deques facilitates removal and insertion at the head and tail of the queue; respectively. In fact, deques support element insertion and removal at both ends.

## Java Deque Interface
The interface called Deque is present in java.util package. 
It is the subtype of the interface queue. The Deque supports the addition as well as the removal of elements from both ends of the data structure. 
Therefore, a deque can be used as a stack or a queue. 
We know that the stack supports the Last In First Out (LIFO) operation, and the operation First In First Out is supported by a queue. 
As a deque supports both, either of the mentioned operations can be performed on it. Deque is an acronym for "double ended queue".

**ArrayDeque class**
We know that it is not possible to create an object of an interface in Java. 
Therefore, for instantiation, we need a class that implements the Deque interface, and that class is ArrayDeque. 
It grows and shrinks as per usage. It also inherits the AbstractCollection class.

The important points about ArrayDeque class are:

* Unlike Queue, we can add or remove elements from both sides.
* Null elements are not allowed in the ArrayDeque.
* ArrayDeque is not thread safe, in the absence of external synchronization.
* ArrayDeque has no capacity restrictions.
* ArrayDeque is faster than LinkedList and Stack.
  
## Java Map Interface
A map contains values on the basis of key, i.e. key and value pair. Each key and value pair is known as an entry. A Map contains unique keys.
A Map is useful if you have to search, update or delete elements on the basis of a key.

Java Map Hierarchy
There are two interfaces for implementing Map in java: Map and SortedMap, and three classes: HashMap, LinkedHashMap, and TreeMap.

A Map doesn't allow duplicate keys, but you can have duplicate values. HashMap and LinkedHashMap allow null keys and values, 
but TreeMap doesn't allow any null key or value.

A Map can't be traversed, so you need to convert it into Set using keySet() or entrySet() method.

**Class	Description**
**HashMap	HashMap** is the implementation of Map, but it doesn't maintain any order.
**LinkedHashMap**	LinkedHashMap is the implementation of Map. It inherits HashMap class. It maintains insertion order.
**TreeMap	TreeMap** is the implementation of Map and SortedMap. It maintains ascending order.

**Sorted Map**

SortedMap is an interface in the collection framework. 
This interface extends the Map interface and provides a total ordering of its elements (elements can be traversed in sorted order of keys). 
The class that implements this interface is TreeMap.

The SortedMap interface is a subinterface of the java.util.Map interface in Java. 
It extends the Map interface to provide a total ordering of its elements, based on the natural order of its keys.

The main difference between a SortedMap and a regular Map is that the elements in a SortedMap are stored in a sorted order, 
whereas in a Map the elements are stored in an arbitrary order. The sorting order is determined by the natural order of the keys, 
which must implement the java.lang.Comparable interface, or by a Comparator passed to the SortedMap’s constructor.

**Hashtable**

Java Hashtable class implements a hashtable, which maps keys to values. It inherits Dictionary class and implements the Map interface.

* A Hashtable is an array of a list. Each list is known as a bucket. The position of the bucket is identified by calling the hashcode() method. A Hashtable contains values based on the key.
* Java Hashtable class contains unique elements.
* Java Hashtable class doesn't allow null key or value.
* Java Hashtable class is synchronized.
* The initial default capacity of Hashtable class is 11 whereas loadFactor is 0.75.

**Difference between Hashmap and Hashtable**
https://www.javatpoint.com/difference-between-hashmap-and-hashtable

##  Java EnumSet
https://www.javatpoint.com/java-enumset

## Java EnumMap
https://www.javatpoint.com/java-enummap








