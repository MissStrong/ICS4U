## Exercise 16-5 Solutions

Create a program that uses a loop to determine which of the monetary values inclusively between 0.00 and 9.99 are inaccurate in the Change assignment. 

Here they are:

0.29 0.57 0.58 1.13 1.14 1.15 1.16 2.01 2.03 2.05 2.07 2.26 2.28 2.30 2.32 2.51 2.53 2.55 4.02 4.06 4.10 4.14 4.27 4.31 4.35 4.39 4.52 4.56 4.60 4.64 4.77 4.81 4.85 4.89 5.02 5.06 5.10 8.03 8.04 8.12 8.20 8.28 8.29 8.37 8.45 8.53 8.54 8.62 8.70 8.78 8.79 8.87 8.95 9.03 9.04 9.12 9.20 9.28 9.29 9.37 9.45 9.53 9.54 9.62 9.70 9.78 9.79 9.87 9.95

Code:

```java
/**
 * Takes an amount that represents a dollar around and returns the minimum
 * number of pennies needed for that amount
 * @param amount
 * @return 
 */
 private static int calculatePennies(String amount) {
    int total, toonies, loonies, quarters, dimes, nickels, pennies;
    double convertIn;
    convertIn = Double.parseDouble(amount)*100;
    total = (int)convertIn;
        
    toonies = total / 200;
    total -= toonies * 200;
    loonies = total / 100;
    total -= loonies * 100;
    quarters = total / 25;
    total -= quarters * 25;
    dimes = total / 10;
    total -= dimes * 10;
    nickels = total / 5;
    total -= nickels * 5;
    pennies = total;
        
    return pennies;
}

/**
 * @param args the command line arguments
 */
public static void main(String[] args) {
    for (int i = 0; i < 1000; i++) {
        double d = i/100.0;
        String amount = Double.toString(d);
        if (calculatePennies(amount) != i % 5) System.out.print(i/100.0 + " ");
    }
}
```
    
