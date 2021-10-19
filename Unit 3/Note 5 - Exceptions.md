## Note – Exceptions

An **exception** is an error that causes a program to end abruptly. We say that exceptions are **thrown** in Java, whereas in some other languages we say that exceptions are *raised*.

In Java, there is an `Exception` class for any type of exception. Here is [the documentation](https://docs.oracle.com/javase/8/docs/api/index.html?java/lang/Exception.html) for the `Exception` class. It has 75 subclasses, including `IOException`.

We saw the `IOException` with file reading. `IOException` is a general class for exceptions that occur due to failed or interrupted I/O processes. Its subclasses include more specific exceptions such as `FileNotFoundException` and `EOFException`.

A `FileNotException` is thrown by the `Scanner()` function when the argument is not a valid `File` object. That's why we can use `catch (IOException e)` to handle the situation when we enter a bad filename.

When we create our own methods, we can throw an exception object using the keyword `throw`. Here is an example.

```java
/**
 * @author MissStrong
 */

public class Main {

  /**
   * Takes a word (a string with only alphabet characters) and returns
   * the number of capital letters in it.
   *
   * @param word
   * @throw IllegalArgumentException when the argument contains any non-alphabet characters
   */
  public static int numberOfCapitalLetters(String word) throws IllegalArgumentException {

    int count = 0; // keeps track of the number of capital letters seen so far
    
    // changes the string into an array of its individual characters and loops through them
    for (char c : word.toCharArray()) {

      // checks whether the character is a letter
      if (Character.isLetter(c)) {
        // checks whether the letter is capital
        if (c == Character.toUpperCase(c)) {
          count++;
        }
      } else {
        // the character is not a letter
        throw new IllegalArgumentException("Every character in the word must be an alphabet charcacter.");
      }
    }

    // the exception was not thrown so we're good to return the count
    return count;
  }
  /**
   * @param args the command line arguments
   */
  public static void main(String[] args) {
    try {
      System.out.println(numberOfCapitalLetters("hello")); // prints 0
      System.out.println(numberOfCapitalLetters("Hello")); // prints 1
      System.out.println(numberOfCapitalLetters("HELLO")); // prints 5
      System.out.println(numberOfCapitalLetters("123")); // throws an error
    } catch (IllegalArgumentException e) {
      System.out.println(e); // catches the error thrown from numberOfCapitalLetters("123")
    }
  } 
} 
```
