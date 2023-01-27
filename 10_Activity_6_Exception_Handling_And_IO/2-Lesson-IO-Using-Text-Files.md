## IO Using Text Files

### I/O

**Input/output** (commonly referred to as **I/O** or **IO**, not to be confused with the domain name *.io*) in computer science refers to the interactions between a program and an external source (e.g. a device, a file, a GUI, etc.).

 
### I/O Using Text Files

In Java, there are several classes that can be used to read files. `Scanner` is one of the most convenient classes to use for parsing text files.

`Scanner` can look at a text file and tell you its content one "word" (i.e. a **token**) at a time or one line at a time. A token is a string of characters that is surrounded by whitespace character on both ends.

In the `Scanner` class, you can use the `hasNext()` and `next()` methods for reading one token at a time, and the `hasNextLine()` and `nextLine()` methods for reading one line at a time. 

 
> Exercise 6-1
>    
> Download and open the [Scanner Example](../Java_Programs/ScannerExample.zip) project. Read through the comment lines to learn what each unfamiliar line of code does.
>    
> To access the input.txt file, go to **Files** (on the same level as **Project** and **Services**) on the left side of the screen and open ScannerExample.
>    
> How could you modify the program so that...
> 1. Every line from the input is printed to the console twice per line? 
>   * Example: `This is line 1. This is is line 1.`
> 2. Every word is printed to the console twice in a row? 
>   * Example: `This This is is line line 1. 1.`
> 3. Every character is printed to the console twice in a row?
>   * Example: `TThhiiss iiss lliinnee 11..`
>   * Hint: Consider using the atChar() method in the String class.
> 4. All space characters are not printed to the console?
>   * Example: `Thisisline1.`
> 5. Every second word is not printed to the console?
>   * Example: `This line`
>    
> Edit: Some of these modifications are tricky without using arrays, which hasn't been taught in this course yet. I didn't realize this until I made the solutions. Sorry about that!
>    
> See solutions [here](../Exercise_Solutions/Exercise-6-1.md).

  
There are several classes to choose from that can be used to write to files. The one I recommend is BufferedWriter.


> Exercise 6-2
>    
> Download and open the [Buffered Writer Example](../Java_Programs/BufferedWriterExample.zip) project. Read through the comment lines to learn what each unfamiliar line of code does.
>    
> To access the output.txt file, go to **Files** (on the same level as **Project** and **Services**) on the left side of the screen and open BufferWritingExample.
>    
> How could you modify the program so that...
> 1. It prints "moo" ten times to cow.txt?
> 2. It prints all the integers inclusively from 0 to 99 to numbers.txt?
> 3. It prints all the characters with ASCII values inclusively between 33 and 126 to characters.txt?
>     
> See solutions [here](../Exercise_Solutions/Exercise-6-2.md).

 
When using any programming language, it is good housekeeping to close any files that you opened soon after you are done using them. This helps prevents the files from getting overwritten or damaged.

In Java 7 and higher, you no longer have to explicitly write `<filename>.close();` since files are automatically closed after they are done being used.
