## Two-Dimensional Arrays

### 2D Arrays

In Java, the term **2D array** is used for arrays whose *elements* are 1D arrays. Essentially, a 2D array is an array within an array. Each inner array represents a row of the 2D array.

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

The notation `[][]` is used for an array of arrays.


### Printing 2D Arrays

You can simulate printing a 2D array by printing its rows individually.

To print the 2D array above, you can do the following.

```java
for (int[] row : grid) {
  System.out.println(Arrays.toString(row));
}
```

