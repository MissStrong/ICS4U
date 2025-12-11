# [Link to Video](https://www.youtube.com/watch?v=tJqeWEXRt4g)

So far we've been using `java.io.Scanner` for reading user input. Although it works and has simple syntax, it is not a good idea to use it when you want your program to run fast.

For contests such as the Canadian Computing Competition, it is highly recommended that you use `java.io.BufferedReader` instead. It makes use of a **buffer** (temporary storage) instead of processing each keystroke as it is typed. According to [DMOJ](https://dmoj.ca/tips/#java-input), `BufferedReader` is 100 times faster than `Scanner`.

You will need the following imports:

* `java.io.BufferedReader`
* `java.io.InputStreamReader`
* `java.io.IOException`

All the examples below need to be in a `try` block where the `catch` block catches an `IOException`.

Here is how to read a single character. The `read()` method returns the ASCII value of a character, so you need to convert it back into a character.

```java
BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // creates the reader
char ch = (char)br.read(); // stores a single character
```

Here is how to read a single line.

```java
BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // creates the reader
String line = br.readLine(); // stores the line into a string
```

Here is how to read multiple tokens within a single line.

```java
BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // creates the reader
String[] tokens = br.readLine().split("\\s+"); // separates a line into tokens
```

Here is how to read an integer, assuming it is on its own line. If there are multiple integers per line, split the line then convert each token into an `int`.

```java
BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // creates the reader
int num = Integer.parseInt(br.readLine()); // converts the string into an integer
```

If you are reading multiple lines and you know how many lines you are expecting, you can read each line one at a time in a *for* loop.
