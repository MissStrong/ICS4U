## Variables and Constants

### Definitions

A **class** is the definition of a data type. For example, the `Math` class provides all the methods that we can use on a string, such as the `random()` method.

An **object** is an instance (i.e. a concrete occurrence) of a class. For example, if we have the string `"Hello World!"` somewhere in our file, it would be a `String` object. 

A **variable** is value that can change over time. 

A **constant** is a value that cannot change over time. Constants in Java should have the modifier `final`, which prevents us from reassigning its value in the same program.

The **scope** of a variable refers to where and when variable can be used.

An **instance variable** is a variable that is declared within a class scope and it may be used anywhere within the object (and outside the object if it has the modifier `public`). It does not have the modifier `static`. Each object may have a different value for this variable.

A **class variable** is a variable that is declared within a class scope and has a shared value among all objects of the class. It has the modifier `static`. 

A **local variable** is a variable that is declared within a local scope. It may be used only within the context (e.g. a method or a loop) it was declared in. It is lost when its context is completed.

A **data type** is the kind of data that a variable can store. Once we declare a variable or constant to be a specific data type, that variable or constant can only store values of that data type. There are many built-in data types, but we can also create our own data types using classes.

All data types are either primitive or composite. A **primitive data type** (a.k.a. a **basic data type**) represents a single piece of information. If a data type isn't primitive, it is a **composite data type**. Whether a data type is primitive or composite depends on the programming language. 

Working with primitive values is usually faster than working with composite values, because Java stores primitive values in a special way that makes memory and speed optimizations possible.

Here are all eight primitive data types in Java. 

| Data Type | Explanation                                                  | Default Value |
| --------- | ------------------------------------------------------------ | ------------- |
| `int`     | Any integer between -2<sup>31</sup> and 2<sup>31</sup>–1 (inclusive). | `0`           |
| `byte`    | Any integer between -2<sup>7</sup> and 2<sup>7</sup>–1 (inclusive). | `0`           |
| `short`   | Any integer between -2<sup>15</sup> and 2<sup>15</sup>–1 (inclusive). | `0`           |
| `long`    | Any integer between -2<sup>63</sup> and 2<sup>63</sup>–1 (inclusive). | `0`           |
| `float`   | Any decimal number that can be represented in 32 bits using IEEE 754. | `0.0f`        |
| `double`  | Any decimal number that can be represented in 64 bits using IEEE 754. | `0.0`         |
| `boolean` | The values `true` or `false`.                                | `false`       |
| `char`    | One Unicode character. It is enclosed in single quotation marks `'`. | `\u0000`      |

When we are mentioning a variable or a constant for the first time, we **declare** it by writing its **data type** and choosing a name for the variable. We can choose to **assign** a value to the variable on the same line as the declaration, or we can choose to do this on a separate line.

For example, these two pieces of code accomplish essentially the same thing.

```java
int height;  // declaration 
height = 10;  // assignment
```
```java
int height = 10;  // declaration and assignment combined
```

If we declare a non-local variable or constant but do not assign a value to it, it will be assigned the data type's default value.  

If we would like to declare more than one variable or constant of the same data type, we may combine them all onto one line. 

For example, these two pieces of code accomplish essentially the same thing.

```java
int height;  
int weight; 
int age;
```

```java
int height, weight, age; // three declarations combined in one line
```
