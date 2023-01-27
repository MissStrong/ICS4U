## Two-Dimensional Arrays

### 2D Arrays

In Java, the term **2D array** is used for arrays whose elements are 1D arrays. Essentially, a 2D array is an array within an array. Each inner array represents a row of the 2D array.

The following grid can be represented using the 2D array `{{1, 2, 3}, {4, 5, 6}, {7, 8, 9}}`.

| 1 | 2 | 3 |
| --- | --- | --- |
| 4 | 5 | 6 |
| 7 | 8 | 9 |


### Initializing 2D Arrays

To initialize the 2D array above, you can do the following.

```java
int[] row0 = {1, 2, 3};
int[] row1 = {4, 5, 6};
int[] row2 = {7, 8, 9};
int[][] grid = {row0, row1, row2};
```

The notation `[][]` is used for an array of arrays.


### Printing 2D Arrays

You can simulate printing a 2D array by printing its rows individually.

To print the 2D array above, you can do the following.

```java
System.out.println(Arrays.toString(row0));
System.out.println(Arrays.toString(row1));
System.out.println(Arrays.toString(row2));
```
 

> Exercise 13-1
>    
> Download and run the [Grid Example](../Java_Programs/GridExample.zip) project. Read the code to learn about how to manipulate the grid above.
> 
> 1. Create a method that returns the result from reversing the rows of a 2D array.
> 
> 2. Create a method that returns the result from reversing the columns of a 2D array.
> 
> Download solutions [here](../Java_Programs/GridExampleSolution.zip).

 
### 2D Arrays in Games

> Exercise 13-2
> 
> Download and run the [Tic Tac Toe](../Java_Programs/TicTacToe.zip) project. Play the game a few times and read the code to see how 2D arrays are implemented.
