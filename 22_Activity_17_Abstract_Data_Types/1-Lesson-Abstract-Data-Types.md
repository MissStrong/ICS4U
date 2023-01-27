## Abstract Data Types

An **abstract data type** (ADT) is a composite data type that is used to store and access data only through specific operations. Its implementation is hidden from the user.


### Choosing an ADT
Choosing the right ADT is an important part of program design. Choosing the right ADT allows your code to be easy to read and efficient; choosing the wrong ADT can be frustrating. Depending on your program, you may not need an ADT at all, or you may want to use more than one ADT.



### Sequence ADT
The **sequence** ADT is an ordered list of elements that can be retrieved and modified. 

These are some the typical operations of a sequence ADT.
* return the length of the sequence
* return the element at a specific index
* insert an element at a particular index and move the elements after it forwards one index
* remove an element at a particular index and move the elements after it backwards one index
* check whether the sequence is empty

If these operations sound familiar, that is because one of the sequence ADTs used in Java is the `ArrayList` class.

Another sequence ADT used in Java is the `Vector` class, which is similar to `ArrayList`, but has some key differences. You don't need to use `Vector` in this course, but you may find it useful to learn a bit about them, since other ADTs are implemented using `Vector`.



### Stack ADT

The **stack** ADT is a collection of elements that are "stacked" on top of each other. Elements get added and removed from the top of the stack. The stack ADT is also known as LIFO (last in, first out) system. 

These are some the typical operations of a stack ADT.
* retrieve the item at the top of the stack
* remove the item at the top of the stack
* add an item to the top of the stack
* check whether the stack is empty

An example of a usage of the stack ADT is your browser history. Every time you visit a new webpage, it gets added to the top of your browser history. Every time you hit "back", it removes the webpage you were just at from the stack, and brings you back to the most previously visited webpage. Of course, you can jump back more than one page at once, which a stack doesn't have to do, but the basic operations of web browsing follow a stack ADT.

Java has a class called `Stack`. You need to import `java.util.Stack` in order to use it. Here are some of its methods. 

| Method | Explanation | Example | Explanation |
| --- | --- | --- | --- |
| `Stack()` | Creates a new (empty) stack. | `Stack<Integer> stackExample = new Stack();` | Creates a new stack of integers called `stackExample`. It is initialized to the empty stack. |
| `empty()` | Returns `true` if the stack is empty, and `false` otherwise. | `stackExample.empty()` | Returns `true`, since `stackExample` is currently empty. |
| `push()` | Adds an elements to the top of the stack. Throws `EmptyStackException` if the stack is empty. | `stackExample.push(1234)` | Adds `1234` to the top of `stackExample`. |
| `peek()` | Returns the top element. Throws `EmptyStackException` if the stack is empty. | `stackExample.peek()` | Returns  `1234`. |
| `pop()` | Removes the top element. Throws `EmptyStackException` if the stack is empty. | `stackExample.pop()` | Removes the top element. Now, `stackExample` is empty again. |

The `Stack` class is integrated using the `Vector` class, so you can also use any methods from `Vector` on a `Stack` object. 

Just like an array list, a queue can contain only one data type, and it cannot be a primitive data type. Each primitive data type has a corresponding class that you can use instead. The main difference between the primitive data type and the class is that a value of the class can be `null`, whereas the value of a primitive data type cannot be `null`.

| Primitive Data Type | Class |
| --- | --- |
| `int` | `Integer`|
| `byte` | `Byte` |
| `short` | `Short`|
| `long` | `Long` |
| `float` | `Float` |
| `double` | `Double` |
| `boolean` | `Boolean` |
| `char` | `Character` |

N.B.: The null character (the one that has ASCII value 0) is different than a value of a character being `null`. If a character is `null`, it's likely because it has not been initialized yet.


### Queue ADT

The **queue** (pronounced like the letter "Q") ADT is a collection of elements that are "lined up", as though they are waiting in line. Elements get added to the back of the queue, and removed from the front of the queue. The stack ADT is also known as FIFO (first in, first out) system. 

These are some the typical operations of a queue ADT.
* retrieve the item at the front of the queue
* remove the item at the front of the queue
* add an item to the back of the queue
* check whether the queue is empty
 
An example of a usage of the queue ADT is prioritizing requests from users when maintaining software. They are typically done on a first-come first-serve basis, although more important request (e.g. vulnerability issues) may "cut in line". 

Java has an **interface** called `Queue`. An interface is typically a category of classes. Classes that fall under the category are said to **implement** the interface. The `PriorityQueue` class, among other classes, implements `Queue`.

You need to import `java.util.Queue` in order to use these classes. Here are some of the methods you can use. 

| Method | Explanation | Example | Explanation |
| --- | --- | --- | --- |
| `PriorityQueue()` | Creates a new (empty) priority queue. | `Queue<Integer> queueExample = new PriorityQueue();` | Creates a new priority queue of integers called `queueExample`. It is initialized to the empty queue. |
| `add()` | Adds an element to the queue, if possible. Returns `true` or throws `IllegalStateException`. | `queueExample.add(1234);` | Adds `1234` to the top of `queueExample`. |
| `offer()` | Adds an element to the queue, if possible. | Returns `true` (success) or `false` (failure). | `queueExample.offer(5678);` | Adds `5678` to the top of `queueExample`. |
| `element()` | Returns the element at the front of the queue or throws `EmptyQueueException` if the queue is empty. | `queueExample.element();` | Returns `5678`. |
| `peek()` | Returns the element at the front of the queue or returns `null` if the queue is empty.| `queueExample.peek();` | Returns `5678`. |
| `remove()` | Returns the element at the front of the queue or throws `NoSuchElementException` if the queue is empty. | 	`queueExample.remove();` | Removes `5678`. Now, `queueExample` contains only `1234`. |
| `poll()` | Returns the element at the front of the queue or returns `null` if the queue is empty. | `queueExample.poll();` | 	`Removes 1234`. Now, queueExample is empty again. |
| `isEmpty()` |	Returns `true` if the queue is empty, and `false` otherwise. | `queueExample.isEmpty()` | Returns `true`, since `queueExample` is currently empty. |



### Deque ADT

The **deque** (pronounced like the word "deck") ADT is a double-ended queue. They are not commonly used, but they could be used in place of a queue or stack.

These are some the typical operations of a deque ADT.
* retrieve the item at the front of the deque
* retrieve the item at the back of the deque
* remove the item at the front of the deque
* remove the item at the back of the deque
* add an item to the front of the deque
* add an item to the back of the deque
* check whether the deque is empty

Java has an interface called `Deque`. The `ArrayDeque` class, among others, implements `Deque`.

You need to import `java.util.Deque` in order to use these classes. Here are some of their methods you can use. 

| Deque Method | Corresponding Queue Method | Corresponding Stack Method |
| --- | --- | --- |
| `addFirst()` | | |
| `addLast()` | `add()` | `push()`|
| `offerFirst()` | | |
| `offerLast()` | `offer()` | |
| `removeFirst()` | `remove()` | |	
| `removeLast()` | | `pop()` |
| `pollFirst()` | `poll()` | |
| `pollLast()` | | |
| `peekFirst()` | `peek()` | |
| `peekLast()` | | `peek()` |
| `getFirst()` | `element()` | |	
| `getLast()` | | |	



### Dictionary ADT

The **dictionary** ADT (also called a **map**, **hash map**, **associative array**, or **hash table**), is an collection of key-value pairs. A value can be quickly retrieved using its corresponding key. Keys are unique and are similar to the idea of an ID in a database. Values do not have to be unique.

These are some the typical operations of a dictionary ADT.
* look up the value of a particular key in the dictionary
* insert a new key-value pair into the dictionary
* remove a key-value pair from the dictionary

Dictionaries have many applications. As the name "dictionary" implies, they can be used as dictionary of words and their definitions. They can also be used to store values that correspond to different traits of an item. For example, your dictionary can contain the key-value pairs `"Name"="Alice"`, `"Gender"="F"`, and `"Age"="40"`, which all correspond to a particular human.

Java has two dictionary ADTs: the `hashMap` class and the `hashtable` class. This example will be using `hashMap`. You need to import `java.util.HashMap` in order to use this class. Here are some of its methods you can use. 

| Method | Explanation | Example | Explanation |
| --- | --- | --- | --- |
| `HashMap()` |	Creates a new (empty) dictionary.	| `HashMap<String, Integer> hashMapExample = new HashMap();` | Creates a new dictionaries called `hashMapExample` in which the keys are strings and the values are integers. |
| `put()` | Adds a new key-value pair into the dictionary. | `hashMapExample.put("a", 1);`</br>`hashMapExample.put("b", 2);` | Adds the key-value pairs `"a"=1` and `"b"=2` to `hashMapExample`. |
| `get()` | Returns the value corresponding to the key, or `null` if the key is not in the dictionary. | `hashMapExample.get("a");` | Returns `1`, which is the value that corresponds to the key `"a"`. |
| `remove()` | Removes the key-value pair from the dictionary. | `hashMapExample.remove("a");` | Removes the key-value pair `"a"=1` from `hashMapExample`. |
| `clear()` | Removes all key-value pairs from the dictionary. | `hashMapExample.clear();` | Removes all the key-value pairs from `hashMapExample`. Now, it is an empty dictionary. |
| `size()` | Returns the number of key-value pairs in the dictionary. | `hashMapExample.size();` | Returns `0`, since `hashMapExample` is empty. |
| `isEmpty()` | Returns `true` is the dictionary is empty, and `false` otherwise. | `hashMapExample.isEmpty();` | Returns `true`, since `hashMapExample` is empty. |
| `containsKey()` | Returns `true` if the dictionary contains the key, and `false` otherwise. | `hashMapExample.containsKey("a");` | Returns `false`, since `hashMapExample` is empty. |
| `containsValue()` | Returns `true` if the dictionary contains the value, and `false` otherwise. | `hashMapExample.containsValue(3)` | Returns `false`, since `hashMapExample` is empty. |

N.B.: In some other programming languages, such as Python, the keys in dictionaries must be immutable data types, which excludes lists. This is not the case for Java; a key can be any data type as long as it isn't primitive.


### Set ADT

The **set** ADT is similar to a mathematical set (or a dictionary with no values) in which every element is unique. It is simply a collection of items. Unlike an unsorted array or an unsorted array list, retrieving an element doesn't require a linear search; it can be retrieved in O(1) time. This is due to the way that sets are stored.

These are some the typical operations of a set ADT. You don't need to know the symbols, although many of you have seen most of them before from a math course, so I've included them for reference.

| Operation | Name in Set Theory | Symbols in Set Theory | Example |
| --- | --- | --- | --- |
| check whether an element is</br>in the set | "element of", "belongs</br>to", "contained in" |	∈ (an element of)</br>∉ (not an element of) | 1 ∈ {1, 2, 3}</br>0 ∉ {1, 2, 3} |
| insert an element into a set | | | |
| the combination of all the</br>elements of the two sets | "union" | ∪  |{1, 2, 3} ∪ {2, 3, 4} = {1, 2, 3, 4} |
| the combination of all the</br>common elements between</br>two sets | "intersection" | ∩ | {1, 2, 3} ∩ {2, 3, 4} = {2, 3} |
| all the elements of a set,</br>excluding the common</br>elements between it and</br>another set | "difference", "relative</br>component" | – | {1, 2, 3} – {2, 3, 4} = {1} |
| check whether all the</br>elements of a set are</br>contained in another set | "subset", "proper subset" | ⊂ (subset)</br>⊆ (proper subset)</br>⊄ (not a subset)</br>⊈ or ⊊ (not a proper subset) | {1, 2, 3} ⊂ {1, 2, 3, 4}</br>{1, 2, 3} ⊆ {1, 2, 3, 4}</br>{1, 2, 3} ⊄ {3, 4, 5}</br>{1, 2, 3} ⊈ {1, 2, 3}</br>{1, 2, 3} ⊊ {1, 2, 3} |
| check whether all the</br>elements of another set are</br>contained in a set | "superset", "proper superset" | ⊃ (superset)</br>⊇ (proper superset)</br>⊅ (not a superset)</br>⊉ or ⊋ (not a proper superset) | {1, 2, 3, 4} ⊃ {1, 2, 3}</br>{1, 2, 3, 4} ⊇ {1, 2, 3}</br>{1, 2, 3} ⊅ {3, 4, 5}</br>{1, 2, 3} ⊉ {1, 2, 3}</br>{1, 2, 3} ⊋ {1, 2, 3} |
| return the number of</br>elements in the set | "cardinality", "size" | \| set \| | \|{1, 2, 3}\| = 3</br>\|{1, 2, 2, 3, 3}\| = 3 |

Java has an interface called `Set`. The `HashSet` class, among others, implements `Set`. You need to import `java.util.Set` in order to use these classes. Here are some of the methods you can use. 


| Method | Explanation | Example | Explanation |
| --- | --- | --- | --- |
| `HashSet()` | Creates a new (empty) set.| `HashSet<Double> hashSetExample = new HashSet();` | Creates a new set called `hashMapExample` that will contain `Double` values. |
| `add()` | Adds a element into the set. | `hashSetExample.add(92.1);`</br>`hashSetExample.add(86.4);` | Adds the elements `92.1` and `86.4` to `hashMapExample`. |
| `contains()` | Returns `true` if the set contains the element, and `false` otherwise. | `hashSetExample.contains(71.9);` | Returns `false`. |
| `remove()` | Removes the element from the set. | `hashSetExample.remove(92.1);` | Removes the element `92.1` from `hashMapExample`. |
| `clear()` | Removes all of the elements from the set. | `hashSetExample.clear();` | Removes all the elements from `hashMapExample`. Now, it is an empty set. |
| `size()` | Returns the number of elements in the set. | `hashSetExample.size();` | Returns `0`, since `hashMapExample` is empty. |
| `isEmpty()` | Returns `true` is the set is empty, and `false` otherwise. | `hashSetExample.isEmpty();` | Returns `true`, since `hashMapExample` is `empty`. |
 

### Hash

The word "hash" has shown up several times in this lesson. Data can be compressed and stored using a **hash function**. This is sometimes called **hashing**. Hash maps, hash tables, and hash sets use hashing to efficiently store and retrieve data.

The number sign # (a.k.a pound sign/key, if you're referring to a telephone) is also sometimes called a hash, but for unrelated reasons. The word "hashtag" from Twitter is related to the name of the symbol #, and unrelated to hashing. 


> Exercise 17-1
> 
> Download and run the [Abstract Data Types Example](../Java_Programs/AbstractDataTypesExamples.zip) project to see how `Stack`, `PriorityQueue`, `ArrayDeque`, `HashMap`, and `HashSet` work.



> Exercise 17-2
> 
> Download and run the [Stack Problem](../Java_Programs/StackProblem.zip) project to see an implementation of a problem that a stack is suitable for. There are two methods that do the same thing: one uses `Stack` and the other does not. The one that uses `Stack` is easier to read and was easier to write.
