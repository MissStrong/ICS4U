## Exercise 16-4 Solutions

What is the result when you run the following lines of code? What can you deduce about how Java treats integer overflow and underflow?

1. `System.out.println(Integer.MAX_VALUE + 1);`

`-2147483648` 

2. `System.out.println(Integer.MIN_VALUE - 1);`

`2147483647`

3. `System.out.println(Integer.MAX_VALUE + Integer.MAX_VALUE);`

`-2`

4. `System.out.println(Integer.MIN_VALUE - Integer.MIN_VALUE);`

`0`

Since `Integer.MAX_VALUE + 1 == Integer.MIN_VALUE` and `Integer.MIN_VALUE - 1 == Integer.MAX_VALUE`, it can be inferred that the integers continue at the other end of the domain when it extends one end. There is no overflow or underflow exception by default.
