## Assignment: Shakespeare

Complete the following assignment and submit your work to the Shakespeare Dropbox.

In this assignment, you will create a program that analyzes text files of Shakespearean plays.

### Instructions

1. Create a new project in NetBeans and call it "Shakespeare".
2. Download all the following text files and place them in the appropriate directory.
  * [Romeo and Juliet](../Java_Projects/romeoAndJulist.txt)
  * [Othello](../Java_Projects/othello.txt)
  * [Macbeth](../Java_Projects/macbeth.txt)
  * [Hamlet](../Java_Projects/hanlet.txt)
3. In the `Shakespeare class,` create the following methods given their documentations and initial line:
```java
/**
 * This method takes a filename and returns the number of times the word "thou" appears in it
 * @param filename a String that represents the name of the text file
 * @return the number of times the word "thou" appears in the text file 
 * @throws java.io.IOException when the input file is missing
 */
public static int thouCount(String filename) throws IOException { ...
```
```java
/**
 * This method replaces all instances of oldWord in oldFilename with newWord in the
 * text file and puts it into newFilename
 * @param oldFilename a String that represents the name of the text file that will be read
 * @param newFilename a String that represents the name of the text file will be written to
 * @param oldWord a String that represents a word that will be replaced
 * @param newWord a String that represents a word that will replace oldWord
 * @throws java.io.IOException when the input file is missing
 */
public static void replaceWord(String oldFilename, String newFilename, String oldWord, String newWord) throws IOException { ...
```
4. Test `thouCount()` by calling it several times under `main` and comparing the results to the numbers you get from using CTRL+F (or ⌘+F if you're using a Mac) on the files to search for the words.
5. Test `replaceWord()` by calling it several times under main and inspecting the content of the new files that are created.
6. When the program works, zip the file and name it **Assignment 6 - \<insert your name here>.zip**.
7. Submit the following to the Dropbox:
  * A .zip file of the program.
  * A .txt file (or a .docx file or a .rtf file) containing all of the code in the .java file.
  * A self-evaluation using the rubric below. 


### Rubric

The following rubric will be used to evaluate your assignment. Each row counts for 4 points, for a total of 16 points. 

You can download the rubric [here](https://docs.google.com/document/d/1vQioLAY71q17v_1i62vbgRaQtkDutPZ6qX3zIZ5WXQo/edit?usp=sharing).

| Category | Level 4 | Level 3 | Level 2 | Level 1 | Below Level 1 |
| --- | --- | --- | --- | --- | --- |
| Knowledge and Understanding  | I demonstrated more than the expected amount of knowledge about file I/O in Java.  | I demonstrated the expected amount of knowledge about file I/O in Java.  | I demonstrated slightly less than the expected amount of knowledge about file I/O in Java.  | I demonstrated a small amount of knowledge about file I/O in Java.  | I demonstrated no knowledge about file I/O in Java. |
| Thinking | I put more than the expected amount of thought and consideration into testing my program. | I put the expected amount of thought and consideration into testing my program. | I put slightly less than the expected amount of thought and consideration into testing my program. | I put a small amount of thought and consideration into testing my program. | I put no thought and consideration into the testing my program. |
| Application | I followed all the instructions and there is a WOW factor. | I followed all the instructions but there is no WOW factor. | I followed most of the instructions. | I followed some of the instructions. | I followed none of the instructions. |
| Communication | The readability and tidiness of my code were beyond the expected quality. | The readability and tidiness of my code met the expected quality. | The readability and tidiness of my code didn't quite meet the expected quality. | The readability and tidiness of my code were far below the expected quality. | My code was not readable nor tidy at all. |
