## Exercise 4-3 Solutions

Using Java, determine whether the following expressions evaluate to `true` or `false`.

1. `!false || true`

`!false || true`    
=> `true || true`     
=> `true`


2. `!(false || true)`

`!(false || true)`     
=> `!(true)`     
=> `false`


3. `(true || false) && (false ^ true)`

`(true || false) && (false ^ true)`    
=> `false && true`    
=> `false`

4. `!((3 < (8 + 4)) && ((4 > 2) ^ (5 != 5)))`

`!((3 < (8 + 4)) && ((4 > 2) ^ (5 != 5)))`    
=> `!((3 < 12) && (true ^ false))`    
=> `!(true && true)`    
=> `!(true)`    
=> `false`

5. `'a' > 'b'`

`'a' > 'b'`    
=> `(int)'a' > (int)'b'`    
=> `97 > 98`    
=> `false`

6. `'A' > 'a'`

`'A' > 'b'`    
=> `(int)'A' > (int)'b'`    
=> `65 > 98`    
=> `false`

7. `'B' > 'a'`

`'B' > 'a'`    
=> `(int)'B' > (int)'a'`    
=> `66 > 98`    
=> `false`
