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
             * If input.txt doesn't exist or can't be read, information about this error
             * gets printed to the output window
             *
             * System.exit(0) is what causes "BUILD SUCCSSFUL" to print to the outut window
             */
            System.out.println("An error occurred.");
            System.out.println(exception);
            System.exit(0);
        } 
    } 
} 

```


When using any programming language, it is good housekeeping to close any files that you opened soon after you are done using them. This helps prevents the files from getting overwritten or damaged.

In Java 7 and higher, you no longer have to explicitly write `<filename>.close();` since files are automatically closed after they are done being used.

