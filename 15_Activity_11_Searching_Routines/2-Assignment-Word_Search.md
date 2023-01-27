## Assignment: Word Search

Complete the following assignment and submit your work to the Word Search Dropbox.

 Google Ngram Viewer is a search engine that can tell you how many times a specific "word" (including acronyms and abbreviations) appears on the world wide web. The data is updated once every year.

In this assignment, you will create a program checks whether a "word" is in the list of the 5000 most common "words" in English on the world wide web, using a text file that contains these 5000 words in alphabetical order.

 
### Instructions

1. Create a new project in NetBeans and call it "Word Search".

2. Download the following text file and place it in the appropriate folder: [5000Words.txt](../Java_Programs/5000Words.txt).

3. In the `Word Search` class, create the following method given its documentation and initial line:
```java
/**
 * This method takes a "word" and uses a binary search algorithm to determine whether it is in the file 5000Words.txt.
 *
 * @param word a String that represents the word you want to check
 * @return true if word is in 5000Words.txt; false otherwise
 * @throws java.io.IOException when the file 5000Words.txt is missing
 */
public static boolean isCommonWord(String word) throws IOException {
```

4. Test `isCommonWord()` by calling it several times under `main` and comparing the result you get from using CTRL+F (or ⌘+F if you're using a Mac) on the file to search for the words.

5. When the program works, zip the file and name it **Assignment 9 - \<insert your name here>.zip**.

6. Submit the following to the Dropbox:
  * A .zip file of the program.
  * A .txt file (or a .docx file or a .rtf file) containing all of the code in the .java file.
  * A self-evaluation using the rubric below. 

### Rubric

The following rubric will be used to evaluate your assignment. Each row counts for 4 points, for a total of 16 points. 

You can download the rubric [here](https://docs.google.com/document/d/1llC__JYzhnRFRFORZDGgXOMHjz04R0Jn8dcYp1kj6LI/edit?usp=sharing).

| Category | Level 4 | Level 3 | Level 2 | Level 1 | Below Level 1 |
| --- | --- | --- | --- | --- | --- |
| Knowledge and Understanding  | I demonstrated more than the expected amount of knowledge about binary search algorithms.  | I demonstrated the expected amount of knowledge about binary search algorithms.  | I demonstrated slightly less than the expected amount of knowledge about binary search algorithms.  | I demonstrated a small amount of knowledge about binary search algorithms.  | I demonstrated no knowledge about binary search algorithms. |
| Thinking | I put more than the expected amount of thought and consideration into testing my program. | I put the expected amount of thought and consideration into testing my program. | I put slightly less than the expected amount of thought and consideration into testing my program. | I put a small amount of thought and consideration into testing my program. | I put no thought and consideration into the testing my program. |
| Application | I followed all the instructions and there is a WOW factor. | I followed all the instructions but there is no WOW factor. | I followed most of the instructions. | I followed some of the instructions. | I followed none of the instructions. |
| Communication | The readability and tidiness of my code were beyond the expected quality. | The readability and tidiness of my code met the expected quality. | The readability and tidiness of my code didn't quite meet the expected quality. | The readability and tidiness of my code were far below the expected quality. | My code was not readable nor tidy at all. |
