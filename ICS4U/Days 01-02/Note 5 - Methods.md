## Note –  Methods

### Review
The following content was in *Note – Introduction to Java*.

> You would have learned about functions in your Grade 11 computer science course. Functions in Java are called methods. A method is a function contained in a class. Since every function in Java is contained in a class, every function in Java is a method.    
>
> When defining a method, you would write the following, in order.    
> 1. `public`, `private`, or `protected` (or leave it blank for package-private)    
> 2. `static` (or leave it blank if it's non-static)    
> 3. the return type (e.g. `int`, `String`, etc.) (or write `void` if the method doesn't return anything)    
> 4. the name of the method    
> 5. the parameters of the method enclosed in parentheses    
> 6. a left curly brace `{`    
> 7. the content of the method    
> 8. a right curly brace `}`    
> At least one class in a package should contain a `main()` method. The content of a `main()` method is run when you run your program. In Java, the `main()` method must be `public`, `static`, and return a `void` value. The `main()` method has the parameter `String[] args` (we'll get to what this means later).      

Let's review functions in a bit more detail. Many of you have already taken, or are currently taking, the Grade 11 math course *Functions* (MCR3U) or *Functions and Applications* (MCF3M).

In math, a relation is a relationship involving one or more variables. A function is a relation in which each independent variable value has only one corresponding dependent variable value.

For example, *f(x) = x<sup>2</sup> + 4* is a function, in which:
* *f* is the name of the function
* *f(x)* is the dependent variable
* *x* is the independent variable
* *x<sup>2</sup> + 4* is how to compute the value of the dependent variable given the value for the independent variable.

Functions can have more than one independent variable. For example, *f(x, y, z) = 4x + 2y - 1/z* is also a function.

Functions in computer science may look different to functions in math, but they are fundamentally similar.


| . | Math Example | Java Example |
| --- | --- | --- |
| Function | f(x, y, z) = 4x + 2y - 1/z | `public static double foo(double x, double y, double z) {`<br></br>&nbsp;&nbsp;&nbsp;&nbsp;`return 4*x + 2*y - 1.0/z;`<br></br>`}` |
| Function name | *f* | `foo` |
| Parameters (Independent Variables) | *x*, *y*, *z* | `x`, `y`, `z` |
| Return Value (Value of Dependent Variable) | *4x + 2y - 1/z* | `4*x + 2*y - 1.0/z` |
| Other Information |  | `public static`: The method is accessible throughout the entire program. <br/></br>`double` (before `foo`): The method returns a double.<br/></br> `double` (before `x`, `y`, and `z`): The parameters `x`, `y`, and `z` are double values. |
| Example | *f(7, -3, 1) = 4(7) + 2(-3) - 1/1 = 28 - 6 - 1 = 21* | `double a = foo(7, -3, 1)`<br/></br>`// the value of a is initialized to 21.0` |
In math, *f*, *g*, and *h* are generic names for functions. In computer science, `foo`, `bar`, and `baz` are generic names for functions. You can also come up with your own dummy names for functions that aren't supposed to be meaningful. I'm quite fond of `bloop`.

In computer science, **parameters** are the variable names used in a method. **Arguments** are the values of the parameters you use when you are calling a method. In the example at the bottom of the previous table, the parameters are x, y, and z, and the arguments are 7, -3, and 1.


### Documenting Methods

You may have been wondering what these recurring lines of code are for:

```java
/**
 * @param args the command line arguments
 */
```

This is the documentation for the `main()` method. It is placed directly above the first line of the `main()` method. It tells the user that `main()` is a method that has one parameter, called `args`, and it represents the command line arguments. 

When we create our own methods, we should document them, too.

```java
/**
 * This method takes the length and width of a rectangle and returns the rectangle's area.
 * @param l the length of the rectangle
 * @param w the width of the rectangle
 * @return the area of the rectangle with length l and width w
 */
```
When you are documenting a method, the following information should be stated:
* A brief description of what the method is for.
* The parameter names and what conditions they have (e.g. can be any integer, must be an integer greater than 2, etc.).
* What the method returns, unless nothing is returned.
* Any side effects of the method (e.g. static variables changing values, information printed to the output window, etc.).

```java
/**
 * This method takes the side lengths of a triangle and returns the triangle's perimeter.
 * @param a the first side length of the triangle
 * @param b the second side length of the triangle
 * @param c the third side length of the triangle
 * @return the perimeter of the triangle with side lengths a, b, and c
 */ 
public static double perimeter(double a, double b, double c) {
    return a + b + c;
}
```
We can call the method above from `main()`.

```java
public static void main() {
    System.out.println(perimeter(4, 2.6, 8.1)); // prints 14.7
}
```

If you don't want a method to be called from a class other than the one it is in, you can use the modifier `private` instead of `public` when you're defining the method.




### Using Built-In Methods

The following content was in *Note – Data Types*.
> The [Java Application Program Interface](https://docs.oracle.com/javase/7/docs/api/) (API) is a collection of prewritten packages, classes, and interfaces. You can use it to find out what packages, classes, and interfaces exist and how you can use them when you are writing code in Java. 
>    
> For example, under **All Classes**, you can find **Math**. Under **Methods Summary**, you can see all its built-in methods. One of the methods is **pow(double a, double b)**. This tells that if you want to evaluate 2<sup>3</sup>, you would use `Math.pow(2, 3)`. (This is an example of coercion, since 2 and 3 are actually integers, not doubles.)


Let's look at some more of the built-in methods in `Math`.
* `Math.max()` compares two values and returns the largest value.
* `Math.pow()` computes and returns the first value to the power of the second value.
* `Math.random()` returns a pseudo-random number that is greater than zero and less than one.
* `Math.round()` rounds a value up or down to the nearest integer and returns the value.
* `Math.sqrt()` computes and returns the square root of a specific number.
* `Math.abs()` finds the absolute value of a number.
* `Math.ceil()` computes and returns the smallest integer greater than, or equal to, the number.
* `Math.floor()` computes and returns the largest integer less than, or equal to, the number.
* `Math.min()` compares two numbers and returns the smallest.

Just like when you created a custom method and called it from a different file, the class name goes before the method name and is separated by a dot.
