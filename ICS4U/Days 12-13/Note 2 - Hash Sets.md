## Hash Sets

### Sets

**Set** is an abstract data type. It is similar to a mathematical set in which every element is unique. It is simply a collection of items. Unlike an unsorted array or an unsorted array list, retrieving an element doesn't require a linear search; it can be retrieved instantaneously. This is due to the way that sets are stored.

These are some the typical operations of a set. You don't need to know the symbols, although many of you have seen most of them before from a math course, so I've included them for reference.

| Operation                                                    | Name in Set Theory                         | Symbols in Set Theory                                        | Example                                                      |
| ------------------------------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| check whether an element is in the set                       | "element of", "belongs to", "contained in" | ∈ (an element of)</br>∉ (not an element of)                  | 1 ∈ {1, 2, 3}</br>0 ∉ {1, 2, 3}                              |
| insert an element into a set                                 |                                            |                                                              |                                                              |
| the combination of all the elements of the two sets          | "union"                                    | ⋃                                                            | {1, 2, 3} ⋃ {2, 3, 4} = {1, 2, 3, 4}                         |
| the combination of all the common elements between two sets  | "intersection"                             | ⋂                                                            | {1, 2, 3} ⋂ {2, 3, 4} = {2, 3}                               |
| excluding the common elements between it and another set     | "difference", "relative component"         | –                                                            | {1, 2, 3} – {2, 3, 4} = {1}                                  |
| check whether all the elements of a set are contained in another set | "subset", "proper subset"                  | ⊂ (subset)</br>⊆ (proper subset)</br>⊄ (not a subset)</br>⊈ or ⊊ (not a proper subset) | {1, 2, 3} ⊂ {1, 2, 3, 4}</br>{1, 2, 3} ⊆ {1, 2, 3, 4}</br>{1, 2, 3} ⊄ {3, 4, 5}</br>{1, 2, 3} ⊈ {1, 2, 3}</br>{1, 2, 3} ⊊ {1, 2, 3} |
| check whether all the elements of another set are contained in a set | "superset", "proper superset"              | ⊃ (superset)</br>⊇ (proper superset)</br>⊅ (not a superset)</br>⊉ or ⊋ (not a proper superset) | {1, 2, 3, 4} ⊃ {1, 2, 3}</br>{1, 2, 3, 4} ⊇ {1, 2, 3}</br>{1, 2, 3} ⊅ {3, 4, 5}</br>{1, 2, 3} ⊉ {1, 2, 3}</br>{1, 2, 3} ⊋ {1, 2, 3} |
| return the number of elements in the set                     | "cardinality", "size"                      | \| set \|                                                    | \|{1, 2, 3}\| = 3</br>\|{1, 2, 2, 3, 3}\| = 3                |

### HashSet

Java has a class called `HashSet`, which can be used as a set. You need to import `java.util.HashSet`in order to use it. Here are some of the methods you can use. 


| Method       | Explanation                                                  | Example                                                     | Explanation                                                  |
| ------------ | ------------------------------------------------------------ | ----------------------------------------------------------- | ------------------------------------------------------------ |
| `HashSet()`  | Creates a new (empty) set.                                   | `HashSet<Double> hashSetExample = new HashSet();`           | Creates a new set called `hashSetExample` that will contain `Double` values. |
| `add()`      | Adds an element into the set.                                | `hashSetExample.add(92.1);`</br>`hashSetExample.add(86.4);` | Adds the elements `92.1` and `86.4` to `hashSetExample`.     |
| `contains()` | Returns `true` if the set contains the element, and `false` otherwise. | `hashSetExample.contains(71.9);`                            | Returns `false`.                                             |
| `remove()`   | Removes the element from the set.                            | `hashSetExample.remove(92.1);`                              | Removes the element `92.1` from `hashSetExample`.            |
| `clear()`    | Removes all of the elements from the set.                    | `hashSetExample.clear();`                                   | Removes all the elements from `hashSetExample`. Now, it is an empty set. |
| `size()`     | Returns the number of elements in the set.                   | `hashSetExample.size();`                                    | Returns `0`, since `hashSetExample` is empty.                |
| `isEmpty()`  | Returns `true` is the set is empty, and `false` otherwise.   | `hashSetExample.isEmpty();`                                 | Returns `true`, since `hashSetExample` is `empty`.           |

Here is an example of some of the things you can do with `HashSet`.

```java
/* Playing aroundwith HashSet */
HashSet<String> myHashSet = new HashSet();

myHashSet.add("boat");
myHashSet.add("car");
myHashSet.add("train");
myHashSet.add("bike");
myHashSet.add("car");

System.out.println("myHashSet: " + myHashSet);

System.out.println("myHashSet.contains(\"bike\"): " + myHashSet.contains("bike"));
System.out.println("myHashSet.contains(\"llama\"): " + myHashSet.contains("llama"));
System.out.println();

System.out.println("myHashSet.isEmpty(): " + myHashSet.isEmpty());
System.out.println("myHashSet.size(): " +  myHashSet.size());
System.out.println();

myHashSet.remove("car");
System.out.println("myHashSet.remove(\"car\")");
System.out.println("myHashSet.size(): " +  myHashSet.size());
System.out.println("myHashSet: " + myHashSet);
System.out.println();

myHashSet.clear();
System.out.println("myHashSet.clear()");
System.out.println("myHashSet: " + myHashSet);
```

