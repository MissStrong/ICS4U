## Note – String Manipulation

### Strings and Loops

Suppose we want to check whether a string contains a particular character.

We can iterate through it character by character using something like this:

```java
String word;
/* Initialize word here */

for (int i = 0; i < word.length(); i++) {
    /* Do something with word.charAt(i), which is the character at index i */
}
```

N.B.: We can't use `word[i]` to access the character at index `i` in Java, although other programming languages allow this. 

For example, if we wanted to check whether the sentence "The quick brown fox jumps over the lazy dog" contains the letter "v", we can do the following:

```java
String sentence = "The quick brown fox jumps over the lazy dog";
boolean sentenceHasV = false;

for (int i = 0; i < sentence.length(); i++) {
    if (sentence.charAt(i) == 'v') sentenceHasV = true;
}
```

There are several methods in the `String` class that are useful for analyzing the characters that are in it.

N.B.: Always assume that strings are case-sensitive when using any programming language.

| Method | Example | Description |
| --- | --- | --- |
| `equals()` | `"monkey".equals("Monkey"); // false` | Checks whether `"monkey"` and `"Monkey"` have the same content. |
| `equalsIgnoreCase()` | `"monkey".equalsIgnoreCase("Monkey"); // true` | Checks whether `"monkey"` and `"Monkey"` have the same content, ignoring any differences in capitalization. |
| `startsWith()` | `"monkey".startsWith("mo"); // true` | Checks whether `"monkey"` begins with `"mo"`. |
| `endWith()` | `"monkey".endsWith("oy"); // false` | Checks whether `"monkey"` ends with `"oy"`. |
| `contains()` | `"monkey".contains("onk"); // true` | Checks whether `"monkey"` contains `"onk"`. |


There are also several methods in the `String` class that are useful for creating strings based on other strings.

| Method | Example | Description |
| --- | --- | --- |
| `trim()` |  `"  monkey    ".trim(); // "monkey"` | Creates a new string with all whitespace at the beginning and end of the string removed. |
| `substring()` | `"monkey".substring(2); // "nkey"`<br></br>`"monkey".substring(1, 3); // "on"` | Creates a new string with the first two characters removed.<br></br>Creates a new string using the characters between index 1 (inclusive) and 3 (exclusive). |
| `toUpperCase()` | `"Monkey".toUpperCase(); // "MONKEY"` | Creates a new string with all lower case letters changed into upper case letters. |
| `toLowerCase()` | `"Monkey".toLowerCase(); // "monkey"` | Creates a new string with all upper case letters changed into lower case letters. |
| `replace()`      | `"abcabc".replace("a", "ef"); //"efbcefbc"`                  | Creates a new string with all occurrences of `"a"` replaced with `"ef"`.                |
| `replaceFirst()` | `"abcabc".replaceFirst("a", "ef"); //"efbcabc"`              |  Creates a new string with the first occurrence of `"a"` replaced with `"ef"`.           |

It is sometimes useful to convert characters to integers (their ASCII value) to check whether they are a certain type of character (e.g. lower case letter, punctuation mark, whitespace, etc.).

To cast a character to an integer, place `(int)` in front of it. 

It may be useful to remember the following ASCII value ranges. We can see the find the full chart by searching "ASCII chart" in an image search engine.

| Range | Characters |
| --- | --- |
| 0 | `null` |
| 1-31 | Stuff we probably won't use |
| 32 | space |
| 33-47 | punctuation marks and symbols |
| 48-57 | numerals |
| 58-64 | more punctuation marks and symbols |
| 65-90	| upper case letters |
| 91-96	| more punctuation marks and symbols |
| 97-122	| lower case letters |
| 123-126	| more symbols |
| 127	| delete (probably won't use) |

For characters in other languages (e.g. letters with accents or characters in different alphabets and writing systems) and other symbols (eg. wingdings and emojis), we can use their [unicode](https://unicode.org/) value.

### String Formatting

Recall the *About Me assignment*. The `main()` method contained strings that use the `replace()` method.

```java
"My name is _.".replace("_", name);
```

Another way to accomplish the same thing would be to use the `format method` in the `String` class.

```java
String.format("My name is %s.", name);
```

The `%s` is a placeholder for `String`. There are placeholders for other data types, too.

| Data Type | Placeholder |
| --- | --- |
| `char` | `%c` |
| `int`, `byte`, `short`, `long` | `%d` |
| `float` | `%e` for scientific notation<br></br>`%f` |
| `String` | `%s` |

We can use multiple placeholders in the same string. The arguments are placed in order that their placeholders appear.

```java
String name;
int age;
/* initialize name and age */
String.format("My name is %s. I am %d years old.", name, age);
```

N.B.: The `^` and `$` metacharacters work best for text files. They are iffy in binary document files such as .docx and .xlsx.
