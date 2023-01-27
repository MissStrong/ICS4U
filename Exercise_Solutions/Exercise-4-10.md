### Exercise 4-10 Solutions

  ```java
for (int i = 1; i != 10; i += 2) {
    doSomething();
}
```

How could prevent the loop above from running indefinitely by modifying only...

1. the condition?

You can change the condition by changing `10` to any odd number greater than 1, or changing the equality operator to be `<=` or `<`.


2. the incrementation?

You can change the incrementation to `i++`.


3. the initialization?

You can change the initialization so that `i` is any even number less than 10.
