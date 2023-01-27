Exercise 16-2 Solutions

Write a Java program for the tribonacci sequence. The tribonacci sequence is like the Fibonacci sequence, except the first three terms are 1, and all other terms are the sum of the three preceding terms.

```java
/** 
 * This method takes an integer n and returns the nth number in the tribonacci sequence.
 * 
 * @param n a positive integer
 * @return the nth tribonacci number; if n isn't a positive integer, it returns -1
 */
public static int tribonacci(int n) {
    if (n < 1) return -1;
    if (n == 1 || n == 2 || n == 3) return 1;
    else return fibonacci(n - 1) + fibonacci(n - 2) + fibonacci(n - 3);
}
```