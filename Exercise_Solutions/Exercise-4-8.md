## Exercise 4-8 Solutions

Insert the following code into the `main` method.
```java
for (int i = 0; i <= 5; i++) {
  System.out.println(i);
}
```
When you run the program, it should print the integers from 0 to 5 in increasing order.

Modify the program to print:

1. The integers from 0 to 10 in increasing order.
```java
// Prints the integers from 0 to 10 in increasing order.
for (int i = 0; i<=10; i++) {
  System.out.println(i);
}
```

2. The even integers from 4 to 10 in decreasing order.
```java
// Prints the even integers from 4 to 10 in decreasing order.
for (int i = 10; i>=4; i--) {
  if (i % 2 == 0) System.out.println(i);
}
```

3. The integer 5 ten times.
```java
// Prints the integer 5 ten times.
for (int i = 0; i<10; i++) {
  System.out.println(5);
}
```
