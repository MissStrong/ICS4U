## Assignment: Pokemon Battle

Complete the following assignment and submit your work to the Pokemon Battle Dropbox.

In this assignment, you'll download a Java program simulating a Pokemon Battle and modify it according to new specifications. The rules of a Pokemon Battle are very simplified: two Pokemon take turns attacking each other until one of them has lost all of their hit points.

You obviously won't be assessed on your knowledge of Pokemon, so don't be too concerned about using accurate information about Pokemon.
 
### Instructions

1. Download the [PokemonBattle](../Java_Programs/PokemonBattle.zip) project and load it into NetBeans.

2. Modify the program according to [this UML diagram](../Images/Pokemon_Battle_UML.png). The current version is on the left, and the new version you'll be making is on the right. Changes in the `Pokemon` class are highlighted in red, to make the changes clearer. Note that *Pokemon* is in italics in the diagram (it might not be easy to tell). For simplicity, not every type of Pokemon from the franchise are included in this program.

  You are also given the following information to incorporate: 

  * When `Pokemon` p1 attacks another `Pokemon` p2, p2's HP goes down by p1's CP, unless p1's type is p2's weakness, in which it goes down by 1.5 times p1's CP (rounding to the nearest integer). For example, if p1's CP is 20 and p2's HP is 100, p2's HP would become either 80 or 70 (if p1's type is p2's weakness) after the attack.

  * `GrassPokemon`: default HP is 100, default CP is 25, weakness is fire.

  * `WaterPokemon`: default HP is 90, default CP is 35, weakness is grass.

  * `FirePokemon`: default HP is 95, default CP is 30, weakness is water.

3. Once you have added all the new classes and modified the `Pokemon` class, modify the body of `main` in the `Battle` class, incorporating the three types of Pokemon. Feel free to make up your own names of Pokemon.

4. When the program works and you have updated and added all the necessary documentation, zip the file and name it Assignment 14 - <insert your name here>.zip.

5. Submit the following to the Dropbox:

  * A .zip file of your program (with all five files).
  * A .txt file (or a .docx file or a .rtf file) containing all of the code in the .java file.
  * A self-evaluation using the rubric below.


### Rubric

The following rubric will be used to evaluate your assignment. Each row counts for 4 points, for a total of 16 points.

You can download the rubric [here](https://docs.google.com/document/d/1LiMgj04qYihMr_0xN_e8ZXUSQMTIkV-HW0DN_cVwgM0/edit?usp=sharing).


| Category | Level 4 | Level 3 | Level 2 | Level 1 | Below Level 1 |
| --- | --- | --- | --- | --- | --- |
| Knowledge and Understanding  | I demonstrated more than the expected amount of knowledge about OOP concepts such as constructors, inheritance, and encapsulation. | I demonstrated the expected amount of knowledge about OOP concepts such as constructors, inheritance, and encapsulation.  | I demonstrated slightly less than the expected amount of knowledge about OOP concepts such as constructors, inheritance, and encapsulation. | I demonstrated a small amount of knowledge about OOP concepts such as constructors, inheritance, and encapsulation. | I demonstrated no knowledge about OOP concepts such as constructors, inheritance, and encapsulation. |
| Thinking | I put more than the expected amount of thought and consideration into testing my program. | I put the expected amount of thought and consideration into testing my program. | I put slightly less than the expected amount of thought and consideration into testing my program. | I put a small amount of thought and consideration into testing my program. | I put no thought and consideration into the testing my program. |
| Application | I followed all the instructions and there is a WOW factor. | I followed all the instructions but there is no WOW factor. | I followed most of the instructions. | I followed some of the instructions. | I followed none of the instructions. |
| Communication | The readability and tidiness of my code were beyond the expected quality. | The readability and tidiness of my code met the expected quality. | The readability and tidiness of my code didn't quite meet the expected quality. | The readability and tidiness of my code were far below the expected quality. | My code was not readable nor tidy at all. |
