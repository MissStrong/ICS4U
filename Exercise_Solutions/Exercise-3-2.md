### Exercise 3-2 Solutions

1. Does Java follow BEDMAS, or does it read mathematical expression from left to right?

It follows BEDMAS. For example `3 + 4 * 2` returns `11` (which is 3 + 8) instead of `14` (which is 7 * 2).
<br></br>

2. Do brackets work as expected in Java when writing a mathematical expression?

Yes, brackets work just like they should in a math expression. For example, `5 * (1 + 4)` returns `25`.
<br></br>

3. What happens when you use the operator `/` on two doubles?

When the operator `/` is used for two doubles, it does standard division. For example, `30.0 / 4.0` returns `7.5`.
<br></br>

4. What happens when you use the operator `/` on one double and one integer?

When the operator `/` is used for one double and one integer, it does standard division. For example, `30.0 / 4` and `30 / 4.0` both return `7.5`.
<br></br>

5. Let `a` and `b` be integers of your choice. Let `c = (b / a)` and `d = (b % a)`. What is the result when you compute `c * a + d`? Why?

Let's try with `a = 4` and `b = 9`. This gives `c = 2` and `d = 1`. The result for `c * a + d` is `2 * 4 + 1 = 9`, which is `b`. This makes sense since 9 divided by 4 is 2 remainder 1.
