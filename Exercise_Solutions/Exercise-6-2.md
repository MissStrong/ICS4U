Exercise 6-2 Solutions

Download and open the [Buffered Writer Example](../Java_Programs/BufferedWriterExample.zip) project. Read through the comment lines to learn what each unfamiliar line of code does.

To access the output.txt file, go to **Files** (on the same level as **Project** and **Services**) on the left side of the screen and open BufferWritingExample.

How could you modify the program so that...

1. It prints "moo" ten times to cow.txt?

```java
try {
  file = new FileWriter("moo.txt");
  buffer = new BufferedWriter(file);
  
  for (int i = 0; i < 10; i++) {
    buffer.write("moo" + " ");
}
```        

2. It prints all the integers inclusively from 0 to 99 to numbers.txt?

```java
try {
  file = new FileWriter("numbers.txt");
  buffer = new BufferedWriter(file);
  
  for (int i = 0; i < 100; i++) {
    buffer.write(i + " ");
  }
}
```

3. It prints all the characters with ASCII values inclusively between 33 and 126 to characters.txt?

```java
try {
  file = new FileWriter("characters.txt");
  buffer = new BufferedWriter(file);

for (int i = 33; i <= 126; i++) {
  buffer.write((char)(i) + " ");
  }
}
```
