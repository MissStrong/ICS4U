## Assignment: ADT Choice

Complete the following assignment and submit your work to the ADT Choice Dropbox.

You will do ones of the four options. This will involve creating two versions of a method.


### Instructions

1. Create a new project in NetBeans and call it "ADTChoice".

2. Complete one of the four options. This will involve creating two methods. Place these two methods into the `ADTChoice` class.

3. Submit the following to the Dropbox:
* A .zip file of your program (with the two methods).
* A .txt file (or a .docx file or a .rtf file) containing all of the code in the .java file.
* A self-evaluation using the rubric below.

### Option 1: Reverse With No Nums

Create two versions of a method that takes a string and returns the reverse of the string with all numbers removed.

The first method uses a stack of characters to reverse the characters, and the second method uses an array or array list to store the reversed characters. Call the first version `reverseWithNoNumsV1()`, and the second version `reverseWithNoNumsV2()`.

Examples:

* `reverseWithNoNumsV1("hello123")` => `"olleh"`

* `reverseWithNoNumsV2("a1 b2 c3")` => `"c b a"`


### Option 2: Even Duplicates

Create two versions of a method that takes a sorted array of integers and returns a boolean indicating whether every element in the array appears an even number of times.

The first method uses a stack or queue, and the second method does not. Call the first version `evenDupesV1()`, and the second version `evenDupesV2()`.

Examples:

* `evenDupesV1({1, 1, 4, 4, 8, 8, 8, 8, 10, 10})` => `true`

* `evenDupesV2({2, 2, 5, 8, 8, 8, 8})` => `false`


### Option 3: Palindrome

Create two versions of a method that takes a string and returns a boolean indicating whether it is a non-case-seneitive palindrome, ignoring all non-alphanumeric characters.

The first method uses a deque, and the second method does not. Call the first version `palindromeV1()`, and the second version `palindromeV2()`.

Examples:

* `palindromeV1("No melon no lemon!")` => `true`

* `palindromeV2("Alabama")` => `false`


### Option 4: No Duplicates

Create two versions of a method that takes an array of arrays of integers (i.e. a 2D array of integers) and returns a boolean indicating whether all of the integers are unique.

The first method uses a set or a dictionary, and the second method does not. Call the first version `noDupesV1()`, and the second version `noDupesV2()`.

Examples:

* `noDupesV1({{1, 2, 3}, {4, 5, 6}})` => `true`

* `noDupesV2({{2, 4}, {4, 6}})` => `false`


### Rubric

The following rubric will be used to evaluate your assignment. Each row counts for 4 points, for a total of 16 points.

You can download the rubric [here](https://docs.google.com/document/d/1bASPHJrdKGgkm-MY7JKyo1WV6AxCCyJkMfPGMbhr98g/edit?usp=sharing).


| Category | Level 4 | Level 3 | Level 2 | Level 1 | Below Level 1 |
| --- | --- | --- | --- | --- | --- |
| Knowledge and Understanding  | I demonstrated more than the expected amount of knowledge about using stacks, queues, deques, dictionaries and/or sets. | I demonstrated the expected amount of knowledge about using stacks, queues, deques, dictionaries and/or sets.  | I demonstrated slightly less than the expected amount of knowledge about using stacks, queues, deques, dictionaries and/or sets. | I demonstrated a small amount of knowledge about using stacks, queues, deques, dictionaries and/or sets. | I demonstrated no knowledge about using stacks, queues, deques, dictionaries and/or sets. |
| Thinking | I put more than the expected amount of thought and consideration into testing my program. | I put the expected amount of thought and consideration into testing my program. | I put slightly less than the expected amount of thought and consideration into testing my program. | I put a small amount of thought and consideration into testing my program. | I put no thought and consideration into the testing my program. |
| Application | I followed all the instructions and there is a WOW factor. | I followed all the instructions but there is no WOW factor. | I followed most of the instructions. | I followed some of the instructions. | I followed none of the instructions. |
| Communication | The readability and tidiness of my code were beyond the expected quality. | The readability and tidiness of my code met the expected quality. | The readability and tidiness of my code didn't quite meet the expected quality. | The readability and tidiness of my code were far below the expected quality. | My code was not readable nor tidy at all. |


