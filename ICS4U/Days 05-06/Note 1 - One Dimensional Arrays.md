## Lesson: One-Dimensional Arrays

### Arrays vs. Lists

Depending on what programming language you used in your Grade 11 computer science course, you would have either learned about **arrays**, **lists**, or both.

Arrays and lists are both data structures that store ordered sets of values, but there are a few major differences between them:
* arrays have fixed lengths; lists are dynamic in length
* arrays could be immutable; lists are always mutable
* arrays tend to have values of one data type; lists tend to allow values of more than one data type

Here is a summary of what lists and arrays are called in various languages.

| Language | List | Array |
| --- | --- | --- |
| C | linked list | array |
| Turing | linked list |	array |
| C++ | list | array |
| C# | list | array |
| Python | list | tuple (pronounced "too-pull") |
| Processing | array list |	array |
| Java | array list	| array |

Java has an `Array` structure and an` ArrayList` structure. This lesson will be on arrays. You'll learn about array lists in a future lesson.

### Declaring and Initializing Arrays

In order to use array methods in a Java program, you need to import the `java.util.Arrays` package.

At the top of the file, put `import java.util.Arrays;` or `import java.util.*;`. The `*` is called a wildcard, and here it is used to import all the classes from `java.util`, which includes `java.util.Arrays`.


There are two common ways to initialize arrays.

1. Declare and initialize the array on the same line.
 Here is an example.

```java
String[] officeCast = {"Michael", "Dwight", "Jim", "Pam", "Stanley", "Phyllis", "Meredith", "Creed", "Kevin", "Oscar", "Angela", "Ryan", "Kelly", "Toby"};
```

2. Declare the array, then fill the elements one by one.
 Here is an example.

```java
String[] officeCast = new String[14];
officeCast[0] = "Michael";
officeCast[1] = "Dwight";
⋮
officeCast[13] = "Toby";
```

In the first example:
* `String[]` indicates that every element in the array will be a string
* `officeCast` is the name of the array
* the fourteen elements of the array are `"Michael"`, `"Dwight"`, ..., and `"Toby"`

In the second example:
* `String[]` indicates that every element in the array will be a string
* `officeCast` is the name of the array
* `new` is the keyword that is used to create a new object, which is an array (you'll learn about this in more detail in a later lesson)
* `String[14]` indicates that there will be fourteen elements in the array
* `officeCast[<index>] = <element value>;` initializes the element at that index (starting at 0) to be that value


When declaring the array separately, you are allowed to put the `[]` before or after the name of the array, and you may also put a space before them.

For example, the following individual lines of code all accomplish the same thing:

`String[] arrayName = new String[10];`    
`String [] arrayName = new String[10];`    
`String arrayName[] = new String[10];`    
`String arrayName [] = new String[10];`


### main(String[] args)

You may have been wondering since the beginning of the course what the `String[] args` in the `main` method means. Now you know: the `main` method takes an array of strings called `args` (short for *arg*uments). When you run Java files using a terminal you can call the `main` method and give it an array of arguments, although you won't be doing that as a part of this course. 

  

### Printing Arrays

If you declare an array called `arrayName` and run `System.out.println(arrayName);`, it will print a hexadecimal value, which indicates the array's address in memory.

In order to print the contents of the array, you can import `java.util.Arrays` and use `System.out.println(Arrays.toString(arrayName));`. 

 

### Accessing Array Elements

The notation for accessing individual elements is the same as assigning values.

To access an element in an array at index `i`, you can use `arrayName[i];`.

 

### Searching Through Arrays

A **standard `for` loop** can be used to iterate through an array by looking at each element one by one.

It would look something like this:

```java
for (int i = 0; i < arrayName.length; i++) {
    // do something with arrayName[i]
}
```

To get the length of an array, use `arrayName.length`. The reason it's `length` and not `length()` is that `length` is an attribute, not a method. You'll learn about this in more detail in a later lesson.

In Java, the index of the first element of every array is 0. In the first iteration, `i` is 0; in the second iteration, `i` is 1; in the third iteration, `i` is 2; and so on until `i` is the last index of the array.

The last index is `arrayName.length - 1` since the first index is 0, which is why `<` is used in the condition instead of `<=`.  Alternatively, you could write `i <= arrayName.length - 1` as the condition, but it's not as nice looking as `i < arrayName.length`.


Another way of iterating through an array in Java is to use an **enhanced `for` loop**.

It would look something like this for an array of strings:

```java
for (String elem : array) {
    // do something with elem
}
```

If you're using an array of another data type, replace `String` with the correct data type.

For example, it would look something like this for an array of booleans:

```java
for (boolean elem : array) {
    // do something with elem
}
```

