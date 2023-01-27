## Note – Loops

A **loop** is a structure that repeatedly executes a specified block of code. This process of repetition is called **iteration**. 

If you wanted to repeat specific lines of code a specific number of times, or until a specific condition is met, you can use a loop to accomplish that.

There are three loop structures in Java: the *while loop*, the *do while loop* and the *for loop*.


### While Loops

You would generally use a *while loop* when you know how to tell when the block of code should stop being running repeatedly.

Here is the general structure of a *while loop*.
```java
while (<condition>) {
    <statement>;
    ⋮
    <statement>;
}
```

A *while loop* does the following.
1. Checks to see whether the condition is met. If it isn't met, the block does not run.
2. If the condition is met, it runs the block of code (the content within the curly braces).
3. Repeats steps 1-2 repeatedly until the condition is no longer met in step 1.


### Do While Loops

A *while loop* checks the condition before running the block of code. If you want the condition to be checked after the block of code is run once, you can use a *do while loop*. 

Here is the general structure of a *do while loop*.
```java
do {
    <statement>;
    ⋮
    <statement>;
} while (<condition>);
```


### For Loops

You would generally use a *for loop* when you know how many times you want the block of code to* run.

Here is the general structure of a *for loop.
```java
for (<initialization>; <condition>; <incrementation>) {
    <statement>;
    ⋮
    <statement>;
}
```

A *for loop* does the following:
1. Performs the initialization. 
2. Checks to see whether the condition is met. If it isn't met, the block doesn't run.
3. If the condition is met, it runs the block of code (the content within the curly braces).
4. Performs the incrementation.
5. Repeats steps 2-4 repeatedly until the condition is no longer met in step 2.


### Break and Continue

At any point in a loop, you can use the keyword `break` to get out of the loop. The keyword `break` is somewhat controversial in computer science since some programmers consider it bad form. I am not one of them. You may use it in this course.

The keyword `continue` is slightly less controversial, but again, I am okay with you using it in this course. When a loop is run and it reaches a `continue`, it skips to the end of the current iteration.


### Nested Loops

A loop that is placed inside another loop is called a **nested loop**.

Here is an example of a nested loop.
```java
for (int i = 0; i <= 9; i++) {
    for (int j = 0; j <=9; j++) {
        System.out.print(i);
        System.out.println(j);
    }
}
```

In this example, the for loop that iterates on `i` would be referred to as the **outer loop**, and the for loop that iterates on `j` would be referred to as the **inner loop**.

If you had a loop inside of a loop, which is already inside another loop, there would be two levels of inner loops.

 


### Infinite Loops

If a condition is never reached, a loop may run indefinitely with no end in sight.

```java
for (int i = 1; i != 10; i += 2) {
    doSomething(); // repeats indefinitely since the condition i != 10 is never reached
}
```