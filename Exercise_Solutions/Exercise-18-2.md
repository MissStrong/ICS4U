## Exercise 18-2

Create several possible constructors for the `Person` class in Exercise 18-1.

```java
public class Person {

    public String name;
    public String gender;
    public int age;
    
    public Person () {
        this.name = "unknown"
        this.gender = "unknown";
        this.age = -1;
    }
    
    public Person (String name) {
        this.name = name;
        this.gender = "unknown";
        this.age = -1;
    }
    
    public Person (String name, String gender) {
        this.name = name;
        this.gender = gender;
        this.age = -1;
    }
    
    public Person (String name, int age) {
        this.name = name;
        this.gender = "unknown;
        this.age = age;
    }
    
    public Person (String name, String gender, int age) {
        this.name = name;
        this.gender = gender;
        this.age = age;
    }
}
```
