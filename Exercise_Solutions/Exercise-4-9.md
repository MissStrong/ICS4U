## Exercise 4-9 Solution

What is the difference between `System.out.print` and `System.out.println`?

`System.out.println` prints a line separator at the end, whereas `System.out.print` does not.

For example, the following code would print `1` and `2` on separate lines and `BUILD SUCCESSFUL` would appear on the following line.

```java
System.out.println(1);
System.out.println(2); 
```

On the other hand, the following code whereas would print `12` and is immediately followed by `BUILD SUCCESSFUL` (i.e. `12BUILD SUCCESSFUL`).

```java
System.out.print(1);
System.out.print(2); 
```
