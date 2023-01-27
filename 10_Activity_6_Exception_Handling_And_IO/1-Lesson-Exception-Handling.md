## Exception Handling


Whenever you run a program that has errors, you may have noticed that NetBeans attempts to tells you what kind of error it is. 

For example, if you try to divide by zero, you get a message in the console saying that there was an **exception** called `java.lang.ArithmeticException`.

![](../Images/Arithmetic_Exception.png)

An exception is a problem that occurs while a program is running. When an exception occurs, the Java runtime "throws" it. When an exception is thrown and your program doesn't "catch" it (i.e. it doesn't handle it), the program terminates abruptly. There are more than 450 kinds of exceptions built into Java; you can view these all on the Java API documentation.

 
In order to avoid a program from terminating abruptly, you should consider possible exceptions that could occur in your methods.

Here is an example of a method that handles a division by zero error.

```java
public static int divideThreeInts(int a, int b, int c) {
    try {
        return a/b/c;
    } catch(ArithmeticException exception) {
        if (b == 0) System.out.println("Error. B cannot be zero.");
        if (c == 0) System.out.println("Error. C cannot be zero.");
        System.exit(0);
        return 0;
    }
}
```

The content in the `try` block is run first. It tries to run the lines in the block; if an exception occurs, the exception is "thrown" and the rest of the block does not run. 

The content in the `catch` block runs only when the exception `ArithmeticException` has been thrown. It "catches" the exception.

The line `System.exit(0);` is used to indicate that the program has successfully run. If `System.exit(1);` is used instead, the program terminates abruptly. Since `return 0;` (0 is a dummy value here) is placed after it, it is actually never reached. If you exclude the `return` statement, NetBeans warns you that a `return` statement is missing and won't let you run your program. (If anyone knows a nicer way to get around this, please let me know.)

If there are more lines of code you want to run regardless of whether the catch block is run, you can use a `finally` block. You'll see an example of a `finally block` in the next lesson: *Lesson -- Input/Output (I/O) Using Text Files*.

  
### NullPointerException

The null pointer exception is one of the most notorious exceptions in Java. The inventor of the null reference, Sir Charles Antony Richard Hoare, once said,

> *"I call it my billion-dollar mistake. It was the invention of the null reference in 1965… This has led to innumerable errors, vulnerabilities, and system crashes, which have probably caused a billion dollars of pain and damage in the last forty years".*

The null pointer exception occurs when a program tries to use an object reference that has a null value. You'll learn more about this in a later lesson.

 
### Creating Custom Exceptions

Sometimes it is useful to create your own exceptions. You'll learn how to do this is a later lesson. 
