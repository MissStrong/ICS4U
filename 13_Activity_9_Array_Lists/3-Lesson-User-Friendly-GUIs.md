## User-Friendly GUIs

You learned how to create a GUI in Activity 3. There are many features you can use in GUIs besides the ones you used for your Change and Sleep Calculator assignments.

Many GUIs do the following by default:

* Don't allow users to submit invalid inputs.
* Don't allow users to type in the output fields.
* Automatically place the curser inside the first text box when the GUI is first constructed.
* Have the default button be different colour than the rest of the buttons.
* Allow users to press ENTER in place of pushing the default button.
 

### Invalid Inputs

In general, you should not trust that the user will follow the instructions. Be prepared for them to do something wrong. For example, if the user enters "February 47th, Year 2018.5", you don't want your program to proceed as if that were a valid date. Display an error message when they do something wrong, or use an more appropriate method of input, such as a spinner.

 
### Disabling Field

To prevent users from editing a specific field, right-click on the field and go to **Customize Code**. Add `OutputField.setEditable(false);` (with `OutputField` being replaced with your name of the output field) to the bottom of the text box that appears. 

 
### Curser Placement

You can use `textBoxName.requestFocus();` (with `textBoxName` being the name of the text box) such as a text field or a text area, to move the curser there. In general, the less the user has to use their mouse, the better. 

   
### Coloured Buttons

You can change the colour of a button by selecting it and changing the **background** field under **Properties**. You can look up the RGB or hex value of the colour you want. The blue colour used in the Jotto assignment has the RGB value (0, 122, 225).

  
### Key Listening

The action listeners you've been using for buttons "listen" for when the button is pressed or released. You can also make them "listen" for a specific key to be pressed or released.

You can allow a used to press ENTER to perform the same action of pressing a button. To do this, select an input field, right-click on it, then go to **Events>Key>keyReleased**. This will create a method called `InputFieldNameKeyReleased()` (with `InputFieldName` being replaced with your name of the input field).

Place the following in the body of the method.
```java
if (evt.getKeyCode() == VK_ENTER) doSomething();
```
You also need to import `static java.awt.event.KeyEvent.*; `in order for this to work.

Replace `doSomething();` with whatever you want to happen when the user hits ENTER when their curser is in that input field. Since you want it to replace a button, you could copy-paste the body of `ButtonNameActionPerformed()`, since you can't easily call `ButtonNameActionPerformed()`.

However, a better option is to put the body of `ButtonNameActionPerformed()` into a **helper method** (a method with the sole purpose of being reused throughout other methods), then call the helper method in `ButtonNameActionPerformed()` and `InputFieldNameKeyReleased()`. Whenever you find yourself copy-pasting code throughout multiple methods, that is a hint that you should be using a helper method instead.

 
> Exercise 9-4
> 
> Improve your Change Exchange GUI from Activity 3 using all of the suggestions above.
> 
> Download solutions [here](../Java_Programs/ChangeVersion2.zip).
