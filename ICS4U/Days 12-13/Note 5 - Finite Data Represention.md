## Finite Data Representation

### Integer Overflow and Underflow

All computers use a fixed number of bits to represent data. This means that there are limits as to what integers a program can use.  

Java uses 32-bit data representation for integers: The lowest integer it can store is –2<sup>31</sup> and the highest integer it can store is 2<sup>31</sup> – 1. You can use `Integer.MAX_VALUE` and `Integer.MIN_VALUE` to obtain these values.

When you try to compute a value beyond this domain, it is called **integer overflow** (beyond `Integer.MAX_VALUE`) or **integer underflow** (beyond `Integer.MIN_VALUE`).



> Fun fact: The Ariane 5 rocket launch in 1996 failed due to an integer overflow error. The rocket self-destructed and the damage cost approximately $370 million USD.
>
> Here is a video of the Ariane 5 Rocket launch: https://www.youtube.com/watch?v=i67ycNPceHc.
>
> You can hear about the technical explanation from 1:02:25-1:05:32 in this talk: https://www.youtube.com/watch?v=6JwEYamjXpA#t=1h2m25s.




### Imprecision of Double and Float

Programming languages tend to be poor at accurately dividing long decimal numbers due to finite data representation. Be aware that if a calculation in any of your programs seems to be off, it might be that your algorithm may be fine and Java simply can't perform the calculation accurately.

