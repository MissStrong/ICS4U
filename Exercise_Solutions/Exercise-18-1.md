## Exercise 18-1

Create a class called Person using the following information:

A `Person` object can be created from the `Person` class.
A `Person` object contains three fields: a `name` (`String`), a `gender` (`String`), and an `age` (`int`).
A `Person` object can be instantiated by providing its `name`, `gender`, and `age`.

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
