## Strings


### Strings and Loops

Suppose you want to check whether a string contains a particular character.

You can iterate through a string character by character using something like this:

```java
String word;
/* Initialize word here */

for (int i = 0; i < word.length(); i++) {
    /* Do something with word.charAt(i), which is the character at index i */
}
```

N.B.: You can't use `word[i]` to access the character at index `i` in Java, although other programming languages allow this. You have to use `word.charAt(i)` instead.

For example, if you wanted to check whether the sentence "The quick brown fox jumps over the lazy dog" contains the letter 'v', you can do the following:

```java
String sentence = "The quick brown fox jumps over the lazy dog";
boolean sentenceHasV = false;

for (int i = 0; i < sentence.length(); i++) {
    if (sentence.charAt(i) == 'v') sentenceHasV = true;
}
```

Now, suppose you want to check whether a specific sentence has a word that starts with the letter 'j'. You could modify the example above, but a cleaner way would be to split the string into an array of strings.

```java
String sentence = "The quick brown fox jumps over the lazy dog";
boolean sentenceHasJWord = false;

String[] words = sentence.split("\\s+");

for (String word : words) {
    if (word.startsWith("j")) sentenceHasJWord = true;
}
```

The `split()` method in the `String` class splits a string based on a pattern and puts the individual parts into an array. The pattern `"\\s+"` is a regular expression that represents all whitespace (e.g. space, tab, etc.), so the new array `words` is `{"The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog"}`.

There are several methods in the `String` class that are useful for analyzing the characters that are in it.

N.B.: Always assume that strings are case-sensitive when using any programming language.

| Method | Example | Description |
| --- | --- | --- |
| `equals()` | `"monkey".equals("Monkey"); // false` | Checks whether `"monkey"` and `"Monkey"` have the same content. |
| `equalsIgnoreCase()` | `"monkey".equalsIgnoreCase("Monkey"); // true` | Checks whether `"monkey"` and `"Monkey"` have the same content, ignoring any differences in capitalization. |
| `startsWith()` | `"monkey".startsWith("mo"); // true` | Checks whether `"monkey"` begins with `"mo"`. |
| `endWith()` | `"monkey".endsWith("oy"); // false` | Checks whether `"monkey"` ends with `"oy"`. |
| `contains()` | `"monkey".contains("onk"); // true` | Checks whether `"monkey"` contains `"onk"`. |

N.B.: The equality operator `==` cannot be used to compare whether two strings are identical. When you use `==` for composite data types, it checks whether they are the same object (i.e. they are stored in the same location in memory).

 

There are also several methods in the `String` class that are useful.

| Method | Example | Description |
| --- | --- | --- |
| `trim()` |  `"  monkey    ".trim(); // "monkey"` | Removes all whitespace at the beginning and end of the string. |
| `substring()` | `"monkey".substring(2); // "nkey"`<br></br>`"monkey".substring(1, 3); // "on"` | Removes the first two characters.<br></br>Keeps only the characters between index 1 (inclusive) and 3 (exclusive). |
| `toUpperCase()` | `"Monkey".toUpperCase(); // "MONKEY"` | Changes all lower case letters to be upper case letters. |
| `toLowerCase()` | `"Monkey".toLowerCase(); // "monkey"` | Changes all upper case letters to be lower case letters. |
| `toCharArray()` | `"monkey".toCharArray(); // {'m', 'o', 'n', 'k', 'e', 'y'}` | Creates a character array of the characters in the string. |
| `replace()` | `"abcabc".replace("a", "ef"); // "efbcefbc"` | Replaces all occurrences of `"a"` with `"ef"`. |
| `replaceFirst()` |	`"abcabc".replaceFirst("a", "ef"); // "efbcabc"` | Replaces the first occurrence of `"a"` with `"ef"`. |


It is sometimes useful to convert characters to integers (their ASCII value) to check whether they are a certain type of character (e.g. lower case letter, punctuation mark, whitespace, etc.).

To cast a character into an integer, place `(int)` in front of it. 

It may be useful to remember the following ASCII value ranges. You can see the find the full chart by searching "ASCII chart" in an image search engine.

| Range | Characters |
| --- | --- |
| 0 | `null` |
| 1-31 | Stuff you probably won't use |
| 32 | space |
| 33-47 | punctuation marks and symbols |
| 48-57 | numerals |
| 58-64 | more punctuation marks and symbols |
| 65-90	| upper case letters |
| 91-96	| more punctuation marks and symbols |
| 97-122	| lower case letters |
| 123-126	| more symbols |
| 127	| delete (probably won't use) |

 

### String Formatting

Recall the *About Me assignment*. The `main` method contained strings that use the `replace()` method.

```java
"My name is _.".replace("_", name);
```


Another way to accomplish the same thing would be to use the `format` method in the `String` class.

```java
String.format("My name is %s.", name);
```

The `%s` is a placeholder for `String`. There are placeholders for other data types, too.

| Data Type | Placeholder |
| --- | --- |
| `char` | `%c` |
| `int`, `byte`, `short`, `long` | `%d` |
| `float`, `double` | `%e` for scientific notation<br></br>`%f` |
| `String` | `%s` |

You can use multiple placeholders in the same string. The arguments are placed in the order that their placeholders appear.

```java
String name;
int age;
/* initialize name and age */
String.format("My name is %s. I am %d years old.", name, age);
```
