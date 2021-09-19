## Note – Regular Expressions

### Regular Expressions

**Regular expressions**, often shortened to **regex** (**reg**ular **ex**pressions) are used to describe patterns in a file or webpage.

When we are searching for a pattern, such as "lines that start with the letter Q or X", we can use a regular expression to accomplish that. When you are using CTRL-F (or ⌘-F for Mac users), there is often an option to use regular expressions.

For example, we can use regular expressions to find patterns in Google Docs. This is what the Find and Replace interface looks like in Google Docs.

![](../Images/Find_And_Replace.png)

| Syntax   | Description                                                  | Example           | Explanation                                                  |
| -------- | ------------------------------------------------------------ | ----------------- | ------------------------------------------------------------ |
| `()`     | Used as standard brackets in expressions.                    |                   |                                                              |
| `\|`     | Used for choices.<br></br>Think of it as an OR operator.     | (T\|t)hou         | Matches "Thou" or "thou".                                    |
| `+`      | Matches the preceding expression one or more times.          | The+              | Matches "The", "Thee", "Theee", etc.                         |
| `*`      | Matches the preceding expression zero or more times.         | Hey*              | Matches "He", "Hey", "Heyy", "Heyyy", etc.                   |
| `?`      | Matches the preceding expression zero or one time.           | Thou(gh)?         | Matches "Thou" and "Though".                                 |
| `{n, m}` | Matches the preceding expression between n and m times.      | No{1,7}           | Matches "No", "Noo", "Nooo", up until "Nooooooo".            |
| `^`      | Matches the start of a line.                                 | ^The              | Matches "The" at the beginning of any line.                  |
| `$`      | Matches the end of a line.                                   | end$              | Matches "end" at the end of any line.                        |
| `.`      | Matches any character.                                       | .at               | Matches occurrences of "at" that have a preceding character. |
| `[...]`  | Matches any character in the square brackets.<br></br>(A\|B\|C) behaves the same way as [ABC] | [bchm]at<br></br> | Matches "bat", "cat", "hat", and "mat".                      |
| `[^...]` | Matches any character not in the square brackets.            | [^p]at            | Matches occurrences of "at" except the ones that have a "p" before it. |
| `\`      | Escape character. Used for characters that belong to syntax. | `\.`              | Matches `.`.                                                 |

Tip: The regular expression `.*` matches any sequence of characters.

N.B.: The `^` and `$` metacharacters work best for text files. They are iffy in binary document files such as .docx and .xlsx.

### Regular Expressions in Java

We can use the `Pattern` and `Matcher` classes to implement regular expressions.

First, we import them.

```java
import java.util.regex.Matcher;
import java.util.regex.Pattern;
```

Then, we can create a `Pattern` using regex (remember to escape the backslashes) and a `Matcher` for the string we want to check the pattern against.

```java
Pattern phoneNumberPattern = Pattern.compile("\\([0-9]{3}\\) [0-9]{3}\\-[0-9]{4}");
System.out.println(phoneNumberPattern); // prints the regex for a phone number: \([0-9]{3}\) [0-9]{3}\-[0-9]{4}

Matcher bciPhoneNumber = phoneNumberPattern.matcher("(519) 885-4620");

if (bciPhoneNumber.find()) {
  System.out.println("The pattern matches.");
} else {
  System.out.println("The pattern doesn't match.");
}
```
