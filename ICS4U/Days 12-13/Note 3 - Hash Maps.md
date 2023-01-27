## Hash Maps

### Dictionaries

The **dictionary**, also called a **map**, **hash map**, **hash table**, **associative array**, is an abstract data type. It is collection of key-value pairs. A value can be quickly retrieved using its corresponding key. Keys are unique and are similar to the idea of an ID in a database. Values do not have to be unique.

These are some the typical operations of a dictionary:

* look up the value of a particular key in the dictionary
* insert a new key-value pair into the dictionary
* remove a key-value pair from the dictionary

Dictionaries have many applications. As the name "dictionary" implies, they can be used as dictionary of words and their definitions. They can also be used to store values that correspond to different traits of an item. 

### HashMap

`HashMap` is a class in Java that behaves like a dictionary. You will need to import `java.util.HashMap` in order to use this class. Here are some of its methods you can use. 

| Method            | Explanation                                                  | Example                                                      | Explanation                                                  |
| ----------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `HashMap()`       | Creates a new (empty) dictionary.                            | `HashMap<String, Integer> hashMapExample = new HashMap();`   | Creates a new dictionary called `hashMapExample` in which the keys are strings and the values are integers. |
| `put()`           | Adds a new key-value pair into the dictionary.               | `hashMapExample.put("a", 1);`</br>`hashMapExample.put("b", 2);` | Adds the key-value pairs `"a"=1` and `"b"=2` to `hashMapExample`. |
| `get()`           | Returns the value corresponding to the key, or `null` if the key is not in the dictionary. | `hashMapExample.get("a");`                                   | Returns `1`, which is the value that corresponds to the key `"a"`. |
| `remove()`        | Removes the key-value pair from the dictionary.              | `hashMapExample.remove("a");`                                | Removes the key-value pair `"a"=1` from `hashMapExample`.    |
| `clear()`         | Removes all key-value pairs from the dictionary.             | `hashMapExample.clear();`                                    | Removes all the key-value pairs from `hashMapExample`. Now, it is an empty dictionary. |
| `size()`          | Returns the number of key-value pairs in the dictionary.     | `hashMapExample.size();`                                     | Returns `0`, since `hashMapExample` is empty.                |
| `isEmpty()`       | Returns `true` is the dictionary is empty, and `false` otherwise. | `hashMapExample.isEmpty();`                                  | Returns `true`, since `hashMapExample` is empty.             |
| `containsKey()`   | Returns `true` if the dictionary contains the key, and `false` otherwise. | `hashMapExample.containsKey("a");`                           | Returns `false`, since `hashMapExample` doesn't have `"a"` as a key. |
| `containsValue()` | Returns `true` if the dictionary contains the value, and `false` otherwise. | `hashMapExample.containsValue(3)`                            | Returns `false`, since `hashMapExample`  doesn't have `3` as a value. |

N.B.: In some other programming languages, such as Python, the keys in dictionaries must be immutable data types, which excludes lists. This is not the case for Java; a key can be any composite data type. Instead of using primitive daya types, you can use their corresponding class name.

| Primitive Data Type | Class       |
| ------------------- | ----------- |
| `int`               | `Integer`   |
| `byte`              | `Byte`      |
| `short`             | `Short`     |
| `long`              | `Long`      |
| `float`             | `Float`     |
| `double`            | `Double`    |
| `boolean`           | `Boolean`   |
| `char`              | `Character` |

Here is an example of some of the things you can do with `HashMap`.

```java
/* Playing with HashMap */
HashMap<String, Integer> myHashMap = new HashMap();

myHashMap.put("a", 1);
myHashMap.put("b", 2);
myHashMap.put("c", 3);

System.out.println("myHashMap: " + myHashMap);

System.out.println("myHashMap.get(\"a\"): " + myHashMap.get("a"));
System.out.println("myHashMap.get(\"b\"): " + myHashMap.get("b"));
System.out.println("myHashMap.get(\"c\"): " + myHashMap.get("c"));
System.out.println("myHashMap.get(\"d\"): " + myHashMap.get("d"));
System.out.println();

System.out.println("myHashMap.containsKey(\"b\"): " + myHashMap.containsKey("b"));
System.out.println("myHashMap.containsValue(4): " + myHashMap.containsValue(4));
System.out.println("myHashMap.isEmpty(): " + myHashMap.isEmpty());
System.out.println("myHashMap.size(): " +  myHashMap.size());
System.out.println();

myHashMap.remove("a");
System.out.println("myHashMap.remove(\"a\")");
System.out.println("myHashMap.size(): " +  myHashMap.size());
System.out.println("myHashMap: " + myHashMap);
System.out.println();

myHashMap.clear();
System.out.println("myHashMap.clear()");
System.out.println("myHashMap: " + myHashMap);
System.out.println();
System.out.println();
```

### Hash

The word "hash" has shown up several times in this course. Data can be compressed and stored using a **hash function**. This is sometimes called **hashing**. Hash maps, hash tables, and hash sets use hashing to efficiently store and retrieve data. 

The number sign # (a.k.a pound sign/key, if you're referring to a telephone) is also sometimes called a hash, but for unrelated reasons. The word "hashtag" from Twitter is related to the name of the symbol #, and unrelated to hashing. 