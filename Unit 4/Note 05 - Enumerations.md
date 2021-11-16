## Note – Enumerations

In Java, an `enum` (short for **enumeration**) is like a class combined with an array. It is used for defining an ordered sequence of constant-like values and can help make programs more readable than using an arrays of constants.

Suppose you have a program that uses the days of the week. One option is to declare each of the days of the week as a constant and place them inside an array:

```java
final int MONDAY = 0, TUESDAY = 1, WEDNESDAY = 2, THURSDAY = 3, FRIDAY = 4, SATURDAY = 5, SUNDAY = 6;

final int[] daysOfTheWeek = {MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY};
```

Here is what it looks like if we use `enum` instead. In repl.it, this block of code has to be placed inside of a class, but in other IDEs it can be placed inside or outside a class.

```java
public enum DayOfTheWeek {
  MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY;
}
```

Since the days of the week are treated like constants, they are written in *screaming snake case* (all capital letters with words separated by underscores). Since enumerations are like classes, the name of an `enum` is written in *Pascal case* (like *camel case*, but all words begin with a capital), just like a class is.

Not only does the program becomes more concise and readable with the use of `enum`, we also don't lose any functionality.

If we want to print all the days of the week followed by its value, we can do this:

```java
for (DayOfTheWeek d : DayOfTheWeek.values() {
  System.out.println(d + ": " + d.ordinal());
}
```
The `values()` function here is similar to getting an array of each day of the week. The `ordinal()` function gets the position it appears in the definition of the `enum`, similar to an index of an array.

If we want to check which day of the week a variable is, we can use a switch statement.

```java
DayOfTheWeek d = DayOfTheWeek.THURSDAY;

switch(d) {
  case MONDAY:
    System.out.println("It's Monday!");
    break;
  case TUESDAY:
    System.out.println("It's Tueday!");
    break;
  case WEDNESDAY:
    System.out.println("It's Wednesday!");
    break;
  case THURSDAY:
    System.out.println("It's Thursday!");
    break;
  case FRIDAY:
    System.out.println("It's Friday!");
    break;
  case SATURDAY:
    System.out.println("It's Saturday!");
    break;
  case SUNDAY:
    System.out.println("It's Sunday!");
    break;
}
```

We don't need to check for the `default` "none of the above" case since if `d` hasn't been initialized yet, there will be a red squiggly line under `switch()` and program won't compile .
