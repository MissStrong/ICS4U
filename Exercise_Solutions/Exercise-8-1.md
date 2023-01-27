## Exercise 8-1 Solutions

The following method takes an array of strings `array` and a String `s`, and returns the number of times `s` appears in `array`. 

```java
/** 
 * This method performs a linear search on an array of Strings and returns the
 * number of times a particular String appears in it.
 * 
 * @param array the array of Strings
 * @param s the String that is being searched for
 * @return the number of times s appears in array
 */
public static int arraySearch(String[] array, String s) {
  int count = 0;
  
  for (String elem : array) {
    if (s.equals(elem)) count++;
  }
  
  return count;
}
```

How could you modify the method so that...
1. It returns a boolean indicating whether `s` is an element in `array`?
```java
/** 
 * This method performs a linear search on an array of Strings and returns
 * whether a particular String appears in it.
 *
 * @param array the array of strings
 * @param s the String that is being searched for
 * @return true if s is in array; false otherwise
 */
public static boolean arrayHasString(String[] array, String s) {
    for (String elem : array) {
        if (s.equals(elem)) return true;
    }
    
    return false;
} 
```

2. It takes an array of integers (instead of an array of strings) and an integer (instead of a string), but otherwise does the same thing as the original? 

```java
/** 
 * This method performs a linear search on an array of ints and returns the
 * number of times a particular int appears in it.
 *
 * @param array the array of ints
 * @param n the int that is being searched for
 * @return the number of times n appears in array
 */
 public static int arraySearch(int[] array, int n) {
    int count = 0;

    for (int elem : array) {
        if (elem == n) count++;
    }

    return count;
    }
```

3. It is the same as 2., except it returns the number of ints that are less than or equal to the integer?

```java
/** 
 * This method performs a linear search on an array of ints and returns the
 * number of elements that are less than or equal to a particular int
 *
 * @param array the array of ints
 * @param n the int that is being compared to the elements
 * @return the number of elements less than or equal to n in array
 */
public static int arraySearch(int[] array, int n) {
    int count = 0;

    for (int elem : array) {
        if (elem <= n) count++;
    }

    return count;
}
```
