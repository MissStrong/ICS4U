## Exercise 9-1 Solutions

Write Java code that checks whether...

1. A string's 5th character is a capital letter.

```java
String s;
/* initialize s */

boolean fifthLetterIsCapital = false;

if ((int)s.charAt(4) <= 65 && (int)s.charAt(4) >= 90) fifthLetterIsCapital = true;
```

2. A string contains only brackets and braces (i.e. {, }, (, ), [, ], <, >).

```java
String s;
/* initialize s */

boolean onlyBrackets = true;

char[] brackets = { '{', '''}, '(', '''), '[', ']', '<', '> };
for (int i = 0; i < s.length(); i++) {
    if (!bracket.contains(s.charAt(i))) onlyBrackets = false;
}
```

3. A string contains at least two characters that are numbers.

```java
String s;
/* initialize s */

boolean twoNums = false;
int count = 0;

for (int i = 0; i < s.length(); i++) {
    if ((int)s.charAt(i) <= 48 && (int)s.charAt(i) >= 57) count++;
}
if (count >= 2) twoNums = true;
```
