# [Link to video.](https://www.youtube.com/watch?v=lmrjGtq1-1A)

### Regular Expressions

Suppose we have a long string and we want to extract every substring that follows a particular pattern. We can do that by repeatedly calling `Match.find()`.

```java
  Pattern phonePattern = Pattern.compile("\\([0-9]{3}\\) [0-9]{3}\\-[0-9]{4}"); // this is the pattern for phone numbers that looks like this: (___) ___-___

  String phoneNumbers = "(519) 885-4620 ~~ (519) 888-9749"; // there are two phone numbers in here we want to extract

  Matcher phoneMatcher = phonePattern.matcher(phoneNumbers);

  while (phoneMatcher.find()) { // this will be true every time there is a match 
    System.out.printf("Found a match starting at %d and ending at %d.\n", phoneMatcher.start(), phoneMatcher.end()); // this will print the indices of the first and last character of each phone number
  } 
```

Since `Match.start()` and `Match.end()` give the beginning and ending index of the substring, we can use them to print each phone number.

```java
  Pattern phonePattern = Pattern.compile("\\([0-9]{3}\\) [0-9]{3}\\-[0-9]{4}"); // this is the pattern for phone numbers that looks like this: (___) ___-___

  String phoneNumbers = "(519) 885-4620 ~~ (519) 888-9749"; // there are two phone numbers in here we want to extract

  Matcher phoneMatcher = phonePattern.matcher(phoneNumbers);

  while (phoneMatcher.find()) { // this will be true every time there is a match 
    System.out.println("Phone number found: " + phoneNumbers.substring(phoneMatcher.start(), phoneMatcher.end())); // this will print the phone numbers
  } 
```
