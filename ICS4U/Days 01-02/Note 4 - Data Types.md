## Note – Data Types

### Definitions

A **class** is the definition of a data type. For example, the `Math` class provides all the methods that you can use on a string, such as the `random()` method.

An **object** is an instance (i.e. a concrete occurrence) of a class. For example, if you have the string `"Hello World!"` somewhere in your file, it would be a `String` object. 

A **variable** is value that can change over time. 

A **constant** is a value that cannot change over time. Constants in Java should have the modifier `final`, which prevents you from reassigning its value in the same program.

The **scope** of a variable refers to where and when variable can be used.

An **instance variable** is a variable that is declared within a class scope and it may be used anywhere within the object (and outside the object if it has the modifier `public`). It does not have the modifier `static`. Each object may have a different value for this variable.

A **class variable** is a variable that is declared within a class scope and has a shared value among all objects of the class. It has the modifier `static`. 

A **local variable** is a variable that is declared within a local scope. It may be used only within the context (e.g. a method or a loop) it was declared in. It is lost when its context is completed.

A **data type** is the kind of data that a variable can store. Once you declare a variable or constant to be a specific data type, that variable or constant can only store values of that data type. There are many built-in data types, but you can also create your own data types using classes.

 

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

When you are mentioning a variable or a constant for the first time, you **declare** it by writing its **data type** and choosing a name for the variable. You can choose to **assign** a value to the variable on the same line as the declaration, or you can choose to do this on a separate line.

For example, these two pieces of code accomplish essentially the same thing.

```java
int height;  // declaration 
height = 10;  // assignment
```
```java
int height = 10;  // declaration and assignment combined
```

If you declare a non-local variable or constant but do not assign a value to it, it will be assigned the data type's default value.  

  

If you would like to declare more than one variable or constant of the same data type, you may combine them all onto one line. 

For example, these two pieces of code accomplish essentially the same thing.

```java
int height;  
int weight; 
int age;
```

```java
int height, weight, age; // three declarations combined in one line
```

### Naming Notations

In different programming languages, there are different rules for naming. Here are some of the common notations used.

| Notation Name    | Example                  | Explanation                                                  |
| ---------------- | ------------------------ | ------------------------------------------------------------ |
| Camel Case       | thisIsCamelCase          | Every word begins with a capital, except for the first word.<br/><br/>All other letters are lowercase. |
| Pascal Case      | ThisIsPascalCase         | Every word begins with a capital.<br/><br/>All other letters are lowercase. |
| Snake Case       | this_is_snake_case       | Every letter is lowercase.<br/><br/>Words are separated with underscores. |
| Caterpillar Case | this-is-caterpillar-case | Every letter is lowercase.<br/><br/>Words are separated with hyphens. |

### Naming Conventions/Rules for Java

* Variable names should begin with a lowercase letter, a dollar sign, or an underscore. (Beginning a variable name with a dollar sign or underscore serves a specific purpose. Google it if you're curious.)
* Variable names should include only letters and numbers (with the exception of a possible dollar sign or underscore at the very beginning).
* Variable names and method names should use **camel case**.
* Constant names should use **screaming snake case**. This is snake case with all letters capitalized. (Think of it as screaming or yelling.)
* Classes should use **Pascal case**.

In general, you should use descriptive names for variables to help create code that is self-explanatory.

### Special Characters

Strings are made up of characters, which are typically letters, numbers, and spaces. There are also special characters, such as tabspace and newline that can appear in strings.

Special characters begin with a backslash `\`.

| Special Character                      | Code |
| -------------------------------------- | ---- |
| tabspace                               | `\t` |
| backspace                              | `\b` |
| carriage return (i.e. enter or return) | `\r` |
| newline                                | `\n` |

Here is an example of how you can use a special character.

```java
// Prints "This is Line 1" on the one line, then "This is Line 2" on the next line
System.out.println("This is Line1\nThis is Line 2");
```

However, ``println()`` is designed to print one line at a time, so it is preferable to do the following instead.

```java
System.out.println("This is Line 1");
System.out.println("This is Line 2");
```

The backslash is called an **escape character**, since it "escapes" the next character.

You can also use the escape character to create strings that contain double quotation marks and characters that contain a single quotation mark.

```java
System.out.println("\""); // Prints a double quotation mark
System.out.println("\"\""); // Prints two double quotation marks
System.out.println('\''); // Prints a single quotation mark
```

To create a string with a backslash, you put an escape character in front of it.

```java
System.out.println("\\"); // Prints a backslash
```

### Type Conversion

A **type conversion** occurs when a value is changed into a value of a different but compatible type. There are two kinds of type conversion: explicit and implicit.

You can use **explicit conversion** (a.k.a. **casting**) by treating a variable of one data type as if it belongs to a different, yet similar, data type. You do this by enclosing the new type in parentheses and placing the name of the variable after the parentheses.

These are all the examples of casting that can be done in Java:

* `short` → `byte` or `char`
* `char` → `byte` or `short`
* `int` → `byte`, `short`, or `char`
* `long` → `byte`, `short`, `char`, or `int`
* `float` → `byte`, `short`, `char`, `int`, or `long`
* `double` → `byte`, `short`, `char`, `int`, `long`, or `float`
* any variable → `String`
* `String` → any variable

Here are some examples of methods used for casting.

```java
int num = Integer.parseInt("6") // this changes the string "6" into the integer 6
String total = Integer.toString(6) // this changes the integer 6 into the string "6"
```

The other kind of type conversion is **implicit conversion** (a.k.a. **coercion**). This is done automatically by Java when a program is running. For example, when a value of one numeric type is assigned to a variable of a different numeric type, the numeric types are implicitly converted to the other numeric types.


### Mathematical Operators

Java has the following built-in mathematical operators. You can use them to manipulate and calculate numeric values.

| Operator | Example              | New Value of `score`                                         |
| -------- | -------------------- | ------------------------------------------------------------ |
| `=`      | `score = 10;`        | Assigns 10 to the value of `score`. This only works when `score` has already been declared. |
| `+`      | `score = score + 2;` | Adds 2 to the value of `score`.                              |
| `-`      | `score = score - 5;` | Subtracts 5 from the value of `score`.                       |
| `*`      | `score = score * 2;` | Multiplies the value of `score` by 2.                        |
| `/`      | `score = score / 5`  | Divides the value of `score` by 5 then takes the dividend.   |
| `%`      | `score = score % 5;` | Divides the value of `score` by 5 then takes the remainder.  |
| `+=`     | `score += 7;`        | Adds 7 to the value of `score`.<br><br/>Essentially equivalent to `score = score + 7;`. |
| `-=`     | `score -= 2;`        | Subtracts 2 from the value of `score`.<br><br/>Essentially equivalent to `score = score - 2;`. |
| `*=`     | `score *= 2;`        | Multiplies the value of `score` by 2<br><br/> Essentially equivalent to `score = score * 2;`. |
| `/=`     | `score /= 2;`        | Divides the value of `score` by 2 then takes the dividend.<br><br/>Essentially equivalent to `score = score / 2`;. |
| `/%`     | `score %= 2;`        | Divides the value of `score` by 2 then takes the remainder.<br><br/>Essentially equivalent to `score = score % 2;.` |
| `++`     | `score++;`           | Adds 1 to the value of `score`.<br><br/>Essentially equivalent to `score = score + 1;` and `score += 1;`. |
| `--`     | `score--;`           | Subtracts 1 from the value of `score`.<br><br/>Essentially equivalent to `score = score - 1;` and `score -= 1;`. |

For other mathematical operators, you would need to use built-in methods from the class called `Math`. 


### Java API

The [Java Application Program Interface (API)](https://docs.oracle.com/javase/7/docs/api/) is a collection of prewritten packages, classes, and interfaces. You can use it to find out what packages, classes, and interfaces exist and how you can use them when you are writing code in Java.

For example, under **All Classes**, you can find **Math**. Under **Methods Summary**, you can see all its built-in methods. One of the methods is `pow(double a, double b)`. This tells that if you want to evaluate 2<sup>3</sup>, you would use `Math.pow(2, 3)`. (This is an example of coercion, since 2 and 3 are actually integers, not doubles.)

