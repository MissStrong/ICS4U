## Note – Writing Plaintext Files

There are several classes to choose from when we are writing to files. The one I recommend is `BufferedWriter`.

```java
/**
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
