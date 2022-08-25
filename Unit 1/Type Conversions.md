### Type Conversion

A **type conversion** occurs when a value is changed into a value of a different but compatible type. There are two kinds of type conversion: explicit and implicit.

We can use **explicit conversion** (a.k.a. **casting**) by treating a variable of one data type as if it belongs to a different, yet similar, data type. We do this by enclosing the new type in parentheses and placing the name of the variable after the parentheses.

These are all the examples of casting that can be done in Java:

* `short` → `byte` or `char`
* `char` → `byte` or `short`
* `int` → `byte`, `short`, or `char`
* `long` → `byte`, `short`, `char`, or `int`
* `float` → `byte`, `short`, `char`, `int`, or `long`
* `double` → `byte`, `short`, `char`, `int`, `long`, or `float`
* any variable → `String`
* `String` → any variable

Here are some examples of methods used for casting:

```java
int num = Integer.parseInt("6"); // this changes the string "6" into the integer 6
String total = Integer.toString(6); // this changes the integer 6 into the string "6"
```

The other kind of type conversion is **implicit conversion** (a.k.a. **coercion**). This is done automatically by Java when a program is running.

Here are some examples of coercion:

```java
double d = 4;  // 4 is an int/long, but it is converted to the double 4.0
String s = "a" + 10;  // 10 is converted to the string "10"
```
