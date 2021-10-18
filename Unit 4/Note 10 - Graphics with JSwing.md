## Note – Graphics with JSwing

### Graphical User Interfaces

A **Graphical User Interface** (GUI, pronounced "gooey") is a way of interacting with a computer. Examples of GUIs include windows, icons, and menus. 

We'll be using JSwing to create GUIs in repl.it.

### JSwing in Repl.it

To make a JSwing program, make sure you select **Java Swing** as the language instead of Java. This will provide an additional window for our graphics to appear.

### JSwing Frames

The graphics window will contain a frame for us to put our graphics on. The data type of a frame in JSwing is called a `JFrame`. We can make a frame display like this:

```Java
// Initializes the frame and puts "Window Name" in the top bar
JFrame frame = new JFrame("Window Name");

// Makes the frame the maximum size on repl.it
frame.setSize(800, 600);

// Makes the background of the frame grey
frame.setLayout(null);

// This line is needed to make the frame appear
frame.setVisible(true);

// Makes the exit button stop the program
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
```

This frame will come with a top bar that provides us with a *minimize* button, an *expand* button, and an *exit* button, just like most other windows on your computer.

To make use of many features in JSwing, we should import the following libraries:

```Java
import javax.swing.*; // This is for the components
import java.awt.*; // This is for the fonts and colours
import java.awt.event.*; // This is for the action listeners
import static java.awt.event.KeyEvent.*; // This is for the key listeners
```

### Screen Coordinates

Before we go into GUI components, it'll be important to know that coordinates in programming are different than coordinates in math. 

In math, 2-dimensional coordinates can be graphed on a Cartesian Plane like this:

![](../../Images/Cartesian_Plane.jpg)

In computer science, we don't use the Cartesian plane for coordinates. Instead, the coordinate system we use looks like this:

![](../..//Images/Coordinate_Plane.jpg)

For example, if we are referring to a specific pixel in an image, we would use this coordinate system instead of the Cartesian plane. 

The idea is that this is similar to how we would refer to cells in a table: The row number followed by column number, with Row 0 Column 0 representing the cell in the top-left corner. This is also similar to how we read in English: left to right, top to bottom.

The coordinate (0, 0) is referred to as the **origin**. When programming, **the origin is always at the top-left corner**. 

In math, the origin is at the center of the Cartesian plane. If we are only using the positive quadrant of the Cartesian plane, the origin is at the bottom-left corner.

### JSwing Components

A frame can have many components on it. Here are some examples:

* Labels
* Text Fields
* Text Areas
* Scrollers
* Buttons
* Checkboxes
* Dropdown Menus
* Sliders

In this example, we'll be focusing on labels, text fields, text areas, scrollers, and buttons. These components have similar built-in methods.

The `setBounds()` method is used to make a component show up in a specific location on the frame. The first two parameters are the *x* and *y* coordinates of the top-left corner of the component and the last two parameters are the *width* (horizontal distance) and *height* (vertical distance) of the component.

The `setFont()` method is to set the font name, font style, and font size fo a component.

**Labels** are used to display a short line of text. They are designed to display only one line of text. Here is an example:

```Java
JLabel prompt = new JLabel("Enter amount: $");
// Top-left corner is at (30, 20)
// Size is 200x50
prompt.setBounds(30, 20, 200, 50);
// Font size is 20
prompt.setFont(new Font(prompt.getFont().getName(), Font.PLAIN, 20));
// Adds label to frame
frame.add(prompt);
```


**Text fields** are boxes designed for users to enter a single line of text into. Here is an example:

```Java
JTextField field = new JTextField("$0.00");
// Top-left corner is at (200, 20)
// Size is 400x50
field.setBounds(200, 20, 400, 50);
// Font size is 20
field.setFont(new Font(field.getFont().getName(), Font.PLAIN, 20));
// Adds text field to frame
frame.add(field);
```

**Text areas** are large boxes designed for users to enter multiple lines of text into. Here is an example:

```Java
JTextArea area = new JTextArea("$0.00");
// Top-left corner is at (200, 20)
// Size is 400x50
area.setBounds(200, 20, 400, 50);
// Font size is 20
area.setFont(new Font(area.getFont().getName(), Font.PLAIN, 20));
// Adds text field to frame
frame.add(area);
```

If we don't want the user to enter text into a text field or text area (i.e. they are being used to just display text), we can use the following code:


```java
field.setEditable(false); // Prevents the user from entering text into the text field
field.setEditable(true); // Allows the user to enter text into the text field
```

We can get the text in a label, text field, and text area using `getText()`,  and we can change the text using `setText`.

``` java
field.setText(field.getText() + "123"); // Adds "123" to the end of the text field
```

We can also add **scrollers** to text areas so that they can display an unlimited amount of text. Here is an example:

```Java
// The first three lines are the same as above
JTextArea area = new JTextArea("$0.00");
area.setBounds(200, 20, 400, 50);
area.setFont(new Font(area.getFont().getName(), Font.PLAIN, 20));
// Makes the vertical scrollbar always show and the horizontal scrollbar never show
JScrollPane scroller = new JScrollPane(JScrollPane.VERTICAL_SCROLLBAR_ALWAYS, JScrollPane.HORIZONTAL_SCROLLBAR_NEVER);
// Makes the size and location of the scroller the same as the text area
scroller.setBounds(200, 20, 400, 50);
// Attaches the scroller to the text area
scroller.setViewportView(amountField);
// Adds the scroller (and not the text area) to frame
frame.add(wordsGuessedScroller);
```

**Buttons** are clickable boxes. 

```Java
JButton calculateButton = new JButton("Calculate");
// Top-left corner is at (425, 500)
// Size is 100x50
calculateButton.setBounds(425, 500, 100, 50);
// Adds button to frame
frame.add(calculateButton);
```

We can enable/disable buttons like this:

```java
calculateButton.setEnabled(false); // disables the button
calculateButton.setEnabled(true); // enables the button
```

### JSwing Action Listeners

An **action listener** is a part of a program that "listens" for a particular to event to happen. For example, it could be waiting for a button to be pressed. We use action listeners to add functionality to buttons.

Here is an example of an action listener:

```Java
JButton clickMeButton = new JButton("Click Me");
// Makes the button do something
clickMeButton.addActionListener(new ActionListener() {  
  public void actionPerformed(ActionEvent e) {
    // Prints the message when the button is clicked
    System.out.println("You clicked the button!")
  }
});
```

### JSwing Key Listeners

Similar to an action listener, key listeners "listen" for a specific key to be pressed or released.

For example, we can allow a user to press ENTER to as a keyboard shortcut for pressing a button. Key listeners are added to components, so the keyboard shortcut will only work when your cursor is in the component with the key listener.

```java
textFieldName.addKeyListener(new KeyAdapter() { 
  public void keyReleased(KeyEvent evt) {
    // VK_Enter is the key code for the ENTER key
    if (evt.getKeyCode() == VK_ENTER) {
      // Do something here
    }
  }
});
```

The full list of key codes is in the Java Docs: https://docs.oracle.com/javase/7/docs/api/java/awt/event/KeyEvent.html.

### JSwing Image Icons

We can use the `ImageIcon` class to display images on `JLabel` and `JButton` objects.

We can use the following code to create an image icon for an image called icon.jpg as long as it's in the same location as *Main.java*.

```java
ImageIcon icon = new ImageIcon("icon.jpg");
```

If the image is in a folder (not in the same location as *Main.java*), we can put "folder_name/" (with the actual name of the folder) in front of the filename. 

```java
ImageIcon icon = new ImageIcon("images/icon.jpg");
```

To place this image onto `JButton` (or `JLabel`) object called `buttonName`, we can use the following code:

```java
buttonName.setIcon(icon);
```

If your button/label and image are the same dimensions, the image should fit perfectly.

To retrieve the current image on a button/label, we can use this:

```java
buttonName.getIcon();
```

To remove an image from a button/label, we can use this:

```java
buttonName.setIcon(null);
```
