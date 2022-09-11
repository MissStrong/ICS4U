## Note – Objects

An **object** is an instance (i.e. a concrete occurrence) of a class. For example, if you have the string `"Hello World!"` somewhere in your program, it would be a `String` object. 

### Constructors
In Java, all objects are instantiated using the class's **contructor method**. The constructor method has the same name as the class (including the initial capital letter) and does not have any return type (not even `void`).

To create an object belonging to a particular class, you often need to use the `new` keyword along with the constructor method. For example, to create an integer array list object, you can use `ArrayList<Integer> intArrayList = new ArrayList()`. 

Some classes have simpler ways of creating objects, without directly calling the constructor. For example, to create a `String` object, you don't need to do `String s = new String();`, you can instantiate and initialize it at the same time: `String s = "12345";`. Some classes have operations that call the constructor method for you. For example, to create an array of integers, you don't do `Array<Integer> intArray = new Array(5);` (this actually won't work), you would do `int[] intArray = int[5]` instead.

Since primitive data types don't belong to any class, you don't need to use the `new` keyword to create them.

If you try `Math m = new Math();`, it will throw an exception. The reason that you cannot create a `Math` object is that the constructor in the `Math` class is `private`. When you create your own classes, you can prevent a user from creating an object belonging to you class by making the class's constructor `private`. By default, every class you create has a `public` constructor with a blank body. Every class has a constructor regardless of whether it is explicitly written in the body of the class.

To refer to an object of class in a method body, you can use the `this` keyword. For example, in a GUI program, you can use `this.setVisible(true);` and `this.setVisible(false);` to hide and unhide the GUI form.

Here is an example of a constructor for a custom class `Person` in a file *Person.java*.

```java
public class Person {

  public String name;
  public String gender;
  public int age;
    
  public Person (String name, String gender, int age) {
    this.name = name;
    this.gender = gender;
    this.age = age;
  }
}
```


### Method Overloading

You can create methods with the same name within a class as long as at least one of these three criteria are met.
* They accept a different number of parameters.
* They accept different types of parameters. (Note: `int`, `long`, `short`, `byte`, `float`, `double` are all the same type: the numeric type). 
* They accept the same number of parameters, as long as the types are in a different order. (This is not recommended.)

For example, 
```java
public void example(int n) {
    System.out.println(n);
}

// This is fine.
public void example(int n, int m) {
    System.out.println(n + " " + m);
}

// This is fine.
public void example(String s) {
    System.out.println(s);
}

// This is not fine. This will get a red squiggly line.
public void example(double d) {
    System.out.prinln(d);
}

```

Constructors can be overloaded just like other methods. Here is an example.
```java
public class Person {

  String name;

  public Person() {
    name = "unknown";
  }

  public Person(String s) {
    name = s;
  }
}
```



### Encapsulation

In order to directly access a **field** (variable or constant) in an object from outside its class, it has to be `public`. However, declaring a variable as `public` allows the user to modify its value. There are two ways to allow a user to access a field in an object from outside of the class, without allowing them to modify its value.

1. **Declare the variable as `final`.**     
This prevents the variable from being modified at all once it is initiated, making it a constant.</br></br>
The `Arrays` class uses this strategy: the `length` field is `final`, which is why you can access it using `arrayName.length`, but can't modify it.

2. **Create a method that obtains the value of the variable**.  
You can declare the variable to be `private`, then create a `public` method that returns the value of the variable.</br></br>
The `ArrayList` classes uses this strategy: it has a `private` field called `size`, but a `public` method called `size()`that returns the value of the `size` field.</br></br>
This concept of data hiding is called **encapsulation**. The "capsule" in this case would be the class.

Here is an example of encapsulation with the `Person` example from before.

```java
public class Person {

  private String name;
    
  public Person() {
    this.name = "unknown";
  }
    
  public Person(String name) {
    this.name = name;
  }
       
  public String getName() {
    return name;
  }
    
  public void setName(String newName) {
    name = newName;
  }
}
```




### Static Methods
A `static` method is a method that belongs to a class, not an object. A `static` method typically takes parameters and performs a routine using the arguments. A non-static method cannot be called in the body of a `static` method.
