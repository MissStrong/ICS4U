## Note – IO Using Text Files

### I/O

**Input/output** (commonly referred to as **I/O** or **IO**, not to be confused with the top-level domain name *.io*) in computer science refers to the interactions between a program and an external source (e.g. a device, a file, a graphic user interface, etc.).


### Reading Text Files

In Java, there are several classes that can be used to read files. `Scanner` is one of the most convenient classes for parsing text files.

`Scanner` can look at a text file and tell you its content one "word" (i.e. a **token**) at a time or one line at a time. A token is a string of characters that is surrounded by whitespace characters on both ends.

In the `Scanner` class, you can use the `hasNext()` and `next()` methods for reading one token at a time, and the `hasNextLine()` and `nextLine()` methods for reading one line at a time. 

```java
/**
 * @author MissStrong
 */

// The program uses all the following classes, so they have to be imported
import java.io.File; 
import java.io.IOException;
import java.util.Scanner; 

public class Main {
    /**
     * @param args the command line arguments
     * @throws java.io.IOException when the input file is missing or not readable
     */
    public static void main(String[] args) throws IOException {
        
        try {
            File inputFile = new File("input.txt"); 
            // scanner is going to scan the content of input.txt
            Scanner scanner = new Scanner(inputFile); 
            
            /* 
             * The hasNextLine() method returns true when there is still at least
             * one more line left in the file.
             */
            while (scanner.hasNextLine()) {
                /* 
                 * The nextLine() method returns the content of the current line
                 * and moves on to the next line 
                 */
                String line = scanner.nextLine();
                System.out.println(line); // prints each line one by one
            }
        } catch(IOException exception) {
            /*
             * If input.txt can't be found or can't be read, information about this error
             * gets printed to the console
             */
            System.out.println("An error occurred.");
            System.out.println(exception);
            System.exit(0); // stops the program without an error message showing up
        } 
    } 
} 

```


When using any programming language, it is good housekeeping to close any files that you opened soon after you are done using them. This helps prevents the files from getting overwritten or damaged.

However, in Java 7 and higher, you no longer have to explicitly write `<filename>.close();` since files are automatically closed after they are done being used.

### Writing Text Files

There are several classes to choose from when you are writing to files. The one I recommend is `BufferedWriter`.

```java
/**
 *
 * @author MissStrong
 */

// The program uses all the following classes, so they have to be imported
import java.io.IOException;
import java.io.BufferedWriter;
import java.io.FileWriter;

public class Main {
    /**
     * @param args the command line arguments
     * @throws java.io.IOException when the output file is not writable
     */
    public static void main(String[] args) throws IOException {
        BufferedWriter buffer = null;
        FileWriter file;
        
        try {
            file = new FileWriter("output.txt");
            // buffer is going to keep track of what will be written to output.txt
            buffer = new BufferedWriter(file);
            // this prints "Hello!" to output.txt
            buffer.write("Hello!");
        } catch(IOException exception) {
            /*
             * If output.txt is not writable, information about this error
             * gets printed to the console
             */
            System.out.println("An error occurred.");
            System.out.println(exception);
            System.exit(0); // stops the program without an error message showing up
        } finally {
            // closing buffer is necessary in order for this program to work
            if (buffer != null) buffer.close();
        } 
    } 
} 
```

