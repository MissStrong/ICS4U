## Note: JSwing

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

![](../..1/Images/Coordinate_Plane.jpg)

For example, if we are referring to a specific pixel in an image, we would use this coordinate system instead of the Cartesian plane. 

The idea is that this is similar to how we would refer to cells in a table: The row number followed by column number, with Row 0 Column 0 representing the cell in the top-left corner. This is also similar to how we read in English: left to right, top to bottom.

The coordinate (0, 0) is referred to as the **origin**. When programming, **the origin is always at the top-left corner**. 

In math, the origin is at the center of the Cartesian plane. If we are only using the positive quadrant of the Cartesian plane, the origin is at the bottom-left corner.

### JSwing Components

A frame can have many components on it. Here are some examples:

* Labels
* Text Fields
* Buttons
* Checkboxes
* Dropdown Menus
* Sliders

In this example, we'll be focusing on text fields, labels, and buttons.

The example below is for a label:

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

The `setBounds()` function is used to make a component show up in a specific location on the frame. The first two parameters are the *x* and *y* coordinates of the top-left corner of the component, and the last two parameters are the *width* (horizontal distance) and *height* (vertical distance) of the component.

The syntax is quite similar for other components:

```Java
JTextField amountField = new JTextField("0.00");
// Top-left corner is at (200, 20)
// Size is 400x50
amountField.setBounds(200, 20, 400, 50);
// Font size is 20
amountField.setFont(new Font(amountField.getFont().getName(), Font.PLAIN, 20));
// Adds text field to frame
frame.add(amountField);
```

```Java
JButton calculateButton = new JButton("Calculate");
// Top-left corner is at (425, 500)
// Size is 100x50
calculateButton.setBounds(425, 500, 100, 50);
// Adds button to frame
frame.add(calculateButton);
```

We can get the text in a label or a text field using `getText()` and we can change the text using `setText`.

For example, this line makes the previous text field blank:

```Java
amountField.setText("");
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

