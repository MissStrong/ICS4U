## Exercise 18-3

Create methods that retrieve the fields for the Person class in Exercise 18-1 and 18-2.

```java
public class Person {

    private String name;
    private String gender;
    private int age;
    
    public Person () {
        this.name = "unknown"
        this.gender = "unknown";
        this.age = -1;
    
    public Person (String name, String gender, int age) {
        this.name = name;
        this.gender = gender;
        this.age = age;
    }
    
    public String getName() {
        return name;
    }
    
    public String getGender() {
        return gender;
    }
    
    public int getAge() {
        return age;
    }
}
```
