## Lesson: Conditionals

### Boolean Expressions

It was mentioned in *Lesson -- Data Types* that a `boolean` is a value that is `true` or `false`. A `boolean` is one of the eight primitive data types, which is why the type is all lowercase. 

A **Boolean expression** is an expression that evaluates to either `true` or `false`. You can create Boolean expressions using **comparison operators**, **equality operators**, and **Boolean operators**.

Here are all the operators you can use in Java to create Boolean expressions.

| Operator Name | Operator Symbol | Category | Example | Explanation |
| --- | --- | --- | --- | --- |
| Less Than | `<` | Comparison Operator | `3 < 5 // true` | 3 is less than 5, so the expression is `true`. |
| Greater Than | `>` | Comparison Operator | `3 > 5 // false` | 3 is not greater than 5, so the expression is `false`. |
| Less Than or Equal To | `<=` | Comparison Operator | `3 <= 5 // true`	| 3 is less than or equal to 5, so the expression is `true`.<br></br> `<=` is supposed to look like the ≤ symbol. |
| Greater Than or Equal To | `>=` | Comparison Operator |	`3 >= 5 // false`	| 3 is neither greater than nor equal to 5, so the expression is false. </br?</br>`>=` is supposed to look like the ≥ symbol.
| Equals | `==` | Equality Operator | `3 == 5 // false` | 3 is not equal to 5, so the expression is false.<br></br>Mixing up `=` and `==` is a notorious error in computer science. This applies to many programming languages, not just Java.
| Not Equals | `!=` | Equality Operator | `3 != 5 // true` | 3 is not equal to 5, so the expression is `true`.<br></br>The exclamation point is commonly used to negate operators (i.e. make them the negative of what they originally are). |
| NOT | `!` | Boolean Operator | `!(3 < 5) // false`	| The statement in the parentheses is `true`, so the expression is the negation of that, which is `false`. |
| AND | `&&` | Boolean Operator | `(3 < 5) && (3 > 5) // false` | At least one of those two statements is `false`, so the expression is `false`.<br></br>There is a similar operator, `&`, called a bitwise operator, which does something completely different. Look it up if you're interested. |
| OR	| `\|` |	Boolean Operator | `(3 < 5) \|\| (3 > 5) // true` | At least one of those two statements is `true`, so the expression is `true`.<br></br>There is a similar operator, `\|`, called a bitwise operator, which does something completely different. Look it up if you're interested.<br></br>The pipe character is typically found above or beside the ENTER key on your keyboard.
| XOR | `^` |	Boolean Operator | `(3 < 5) ^ (3 > 5) // true` | Exactly one of those two statements is `true`, so the expression is `true`.<br></br>XOR is called "exclusive OR". It's like OR, except it returns `false` when more than one statement is `true`.<br></br>The `^` symbol is called a "caret", not to be confused with "carrot" or "carat". |

The convention to write the names of Boolean Operators in all capital letters. That's why NOT, AND, OR, and XOR are in all capital letters.

The comparison operators can also be used with `char` values.  It compares them based on character order (which is sort of like alphabetical order, except it compares the ASCII values). The comparison operators cannot be used for `String` values.

> Exercise 4-3
>    
> Using Java, determine whether the following expressions evaluate to `true` or `false`.    
> 1. `!false || true`
> 2. `!(false || true)`
> 3. `(true || false) && (false ^ true)`
> 4. `!((3 < (8 + 4)) && ((4 > 2) ^ (5 != 5)))`
> 5. `'a' > 'b'`
> 6. `'A' > 'a'`
> 7. `'B' > 'a' `
>    
> See solutions [here](../Exercise_Solutions/Exercise-4-3.md).

 
### Conditional Statements

Boolean expressions are often used to check conditions. For example, you may want different blocks of code to run depending on the values of specific variables at specific times.

There are two kinds of conditional statements in Java: the *if* statement and the *switch* statement. 

 
### If Statements

Here is the general structure of an *if* statement.
```java
if (<condition>) {
    <statement>;
    ⋮
    <statement>;
} else if {
    <statement>;
    ⋮
    <statement>;
} else {
    <statement>;
    ⋮
    <statement>;
}
```
The keywords `if`, `else if`, and `else` are hopefully self-explanatory.
* The `if` block runs only if the condition is `true`. 
* Any `else if` blocks run only if all the previous conditions in the conditional structure are `false` (the "else" in `else if`) and the new condition is true (the "if" in else if).
* The `else` block runs only if all the previous conditions in the conditional structure are `false`.

In any conditional structure, you may have as many or as few `else if` blocks as you wish. You may have no more than one `else` block. 

In general, if the conditions are mutually exclusive (i.e. they can't hold true at the same time), you should use `if` followed by `else if` rather than `if` followed by another `if`.

 
If there is only one statement in a block, you may remove the curly braces and move the statement up one line.

For example, the following two pieces of code perform essentially the same thing.

```java
if (y < 10) {
    y++;
}
```

```java
if (y < 10) y++;
```


> Exercise 4-4
>    
> Modify the following code to make it work as expected.    
```java
/**
 * This method takes an integer and prints its smallest prime factor less than 8.
 * @param n a positive integer
 */
public static void findSmallestPrimeFactor(int n) {
    if (n % 2 == 0) {
        System.out.println("2 is the smallest prime factor of " + Integer.toString(n));
    } else if (n % 3 == 0) {
        // Figure out what goes here
    } else if (/* Figure out what goes here */){ 
       // Figure out what goes here
    } else if (/* Figure out what goes here */){ 
        // Figure out what goes here
    } else {
       System.out.println(Integer.toString(n) + " has no prime factors between 2 and 8.");
    }
}        
```
> See solutions [here](../Exercise_Solutions/Exercise-4-4.md).

   
### Switch Statements

Switch statements are conditional structures that are sometimes convenient to use when the condition involves checking equality.

These two pieces of code accomplish essentially the same thing. 

**If Statement**
```java
// provinceName is a Canadian province or territory's two-letter abbreviation
String provinceName = "BC";

// regionName is the province or territory's category using the four-region model
String regionName;

if ((provinceName.equals("BC")) || (provinceName.equals("AB")) || (provinceName.equals("SK")) || (provinceName.equals("MB"))) regionName = "Western Canada";
else if ((provinceName.equals("ON")) || (provinceName.equals("QC"))) regionName = "Central Canada"
else if ((provinceName.equals("NB")) || (provinceName.equals("PE")) || (provinceName.equals("NS")) || (provinceName.equals("NL"))) regionName = "Atlantic Canada";
else if ((provinceName.equals("YT")) || (provinceName.equals("NT")) || (provinceName.equals("NU"))) regionName = "Northern Canada";
else regionName = "Not a region in Canada";
```

**Switch Statement**
```java
// provinceName is a Canadian province or territory's two-letter abbreviation
String provinceName = "BC";

// regionName is the province or territory's category using the four-region model
String regionName;

switch(provinceName) {
    case "BC":
    case "AB":
    case "SK":
    case "MB":
        regionName = "Western Canada";
        break;
    case "ON":
    case "QC":
        regionName = "Central Canada";
        break;
    case "NB":
    case "PE":
    case "NS":
    case "NL":
        regionName = "Atlantic Canada";
        break; 
    case "YT":
    case "NT":
    case "NU":
        regionName = "Northern Canada";
        break;
    default:
        regionName = "Not a region in Canada";
}
```

Notice how `provinceName.equals("BC")` is used instead of `provinceName == "BC"`. This is because the `==` operator for `String` values in Java checks whether they have the same address (i.e. they are the same object). To check whether the content of `provinceName` is `"BC"`, you need to use the `equals()` method.

Notice how you don't need curly braces for each `case` in the *switch* example. This is because the entire *switch* block is run until it reaches a `break` or the end of the *switch* structure. You'll be seeing another use of the keyword `break` in the next lesson: *Lesson -- Loops*.

It is convention to put `default` after all the other cases, since the Java runtime reads it last anyway.

> Exercise 4-5
>    
> You can play around with the code for the *switch* statement example [here](../Java_Programs/SwitchExample.zip).
> 1. What happens when you add a `break` in the `default` statement?
> 2. What happens when you move the `default` statement (with the `break`) higher in the *switch* structure?
> 3. What happens when you move the `default` statement (without the `break`) higher in the *switch* structure? 
>    
> See solutions [here](../Exercise_Solutions/Exercise-4-5.md).

> Exercise 4-6
>    
> Modify the *if* statement to match the *switch* statement.    
>    
> **If Statement**
```java
String dayName = "Thursday";
int dayNum;

if (dayName.equals("Monday")) dayNum = 0;
    /*
     *
     * Figure out what goes here
     *
     *
     */
else dayNum = "Not a day number";
```
> **Switch Statement**
```java
String dayName = "Thursday";
int dayNum;

switch(dayNum) {
    case "Monday":
        dayNum = 0;
        break;
    case "Tuesday":
        dayNum = 1;
        break;
    case "Wednesday":
        dayNum = 2;
        break;
    case "Thursday":
        dayNum = 3;
        break;
    case "Friday":
        dayNum = 4;
        break;
    case "Saturday":
        dayNum = 5;
        break;
    case "Sunday":
        dayNum = 6;
        break;
    default: 
        dayName = "Not a day number";
}
```
> See solutions [here](../Exercise_Solutions/Exercise-4-6.md).
