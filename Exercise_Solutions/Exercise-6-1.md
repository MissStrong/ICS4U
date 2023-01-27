## Exercise 6-1 Solutions

Download and open the (Scanner Example)[../Java_Programs/ScannerExample.zip] project. Read through the comment lines to learn what each unfamiliar line of code does.

To access the input.txt file, go to **Files** (on the same level as **Project** and **Services**) on the left side of the screen and open ScannerExample.

How could you modify the program so that...

1. Every line from the input is printed to the console twice per line? 
  * Example: `This is line 1. This is is line 1.`
  
```java
while (scanner.hasNextLine()) {
  String line = scanner.nextLine();
  System.out.print(line + " ");
  System.out.println(line + " ");
}
```

2. Every word is printed to the console twice in a row? 
  * Example: `This This is is line line 1. 1.`

```java
while (scanner.hasNextLine()) {
  String line = scanner.nextLine();
  String[] words = line.split("\\s+");
  
  for (String word : words) {
    System.out.print(word + " ");
    System.out.print(word + " ");
  }
  
  System.out.println();
}
```

3. Every character is printed to the console twice in a row?
  * Example: `TThhiiss iiss lliinnee 11..`
  * Hint: Consider using the `atChar()` method in the `String` class.

```java
while (scanner.hasNextLine()) {
  String line = scanner.nextLine();
  
  for (int i = 0; i < line.length(); i++) {
    System.out.print(line.charAt(i));
    System.out.print(line.charAt(i));
  }
  
  System.out.println();
}
```


4. All space characters are not printed to the console?
  * Example: `Thisisline1.`

```java
while (scanner.hasNextLine()) {
  String line = scanner.nextLine();
  
  for (int i = 0; i < line.length(); i++) {
    if (line.charAt(i) != ' ') System.out.print(line.charAt(i));
  }
                
  System.out.println();
}
```

5. Every second word is not printed to the console?
  * Example: `This line`

```java
while (scanner.hasNextLine()) {
  String line = scanner.nextLine();
  String[] words = line.split("\\s+");
                
  for (int i = 0; i < words.length; i += 2) {
    System.out.print(words[i] + " ");
  }
                
  System.out.println();
 }
```
