## Exercise 4-6 Solutions

Modify the *if* statement to match the *switch* statement. 

**If Statement**
```java
String dayName = "Thursday";
int dayNum;

if (dayName.equals("Monday")) dayNum = 0;
else if (dayName.equals("Tuesday")) dayNum = 1;
else if (dayName.equals("Wednesday")) dayNum = 2;
else if (dayName.equals("Thurssday")) dayNum = 3;
else if (dayName.equals("Friday")) dayNum = 4;
else if (dayName.equals("Saturday")) dayNum = 5;
else if (dayName.equals("Sunday")) dayNum = 6;
else dayNum = "Not a day number";
```

**Switch Statement**
```java
String dayName = "Thursday";
int dayNum;

switch(dayNum) {
  case "Monday":
    dayNum = 0;
    break;
  case "Tuesday":
    dayNum = 1;
    break;
  case "Wednesday":
    dayNum = 2;
    break;
  case "Thursday":
    dayNum = 3;
    break;
  case "Friday":
    dayNum = 4;
    break;
  case "Saturday":
    dayNum = 5;
    break;
  case "Sunday":
    dayNum = 6;
    break;
  default: 
    dayName = "Not a day number";
}
```
