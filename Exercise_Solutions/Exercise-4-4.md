# Exercise 4-4 Solutions

Modify the following code to make it work as expected.

```java
/**
 * This method takes an integer and prints its smallest prime factor less than 8.
 * @param n a positive integer
 */
public static void findSmallestPrimeFactor(int n) {
	if (n % 2 == 0) {
		System.out.println("2 is the smallest prime factor of " + Integer.toString(n));
	} else if (n % 3 == 0) {
		System.out.println("3 is the smallest prime factor of " + Integer.toString(n));
	} else if (n % 5 == 0) {
		System.out.println("5 is the smallest prime factor of " + Integer.toString(n));
	} else if (n % 7 == 0) {
		System.out.println("7 is the smallest prime factor of " + Integer.toString(n));
	} else {
		System.out.println(Integer.toString(n) + " has no prime factors between 2 and 8.");
	}
}
```
