### Exercise 4-5 Solutions

You can play around with the code for the *switch* structure example [here](../Java_Programs/SwitchExample.zip).

1. What happens when you add a `break` in the `default` statement?

Nothing changes. The `default` statement is read last, so the runtime is about to break out of the structure anyway.


2. What happens when you move the `default` statement (with the `break`) higher in the *switch* structure?

Nothing changes. The `default` statement is read last no matter where it is in the *switch* structure. In general, it's better practice to place it at the bottom to avoid confusing readers who are unaware of this.


3. What happens when you move the `default` statement (without the `break`) higher in the *switch* structure? 

The default statement is performed, but then the rest of the *switch* structure underneath `default` runs again until it reaches a `break` or the end of the structure.
