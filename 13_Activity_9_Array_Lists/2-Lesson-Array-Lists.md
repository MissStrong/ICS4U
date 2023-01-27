## Array Lists

The `ArrayList` class is like a more versatile version of the `Arrays` class. Not only can the length/size of an array list change, there are many convenient built-in methods that can be used. In general, array lists are more favourable than arrays in Java.

Here is a comparison of some of the ways to use arrays and array lists in Java.

| | Arrays | Array Lists |
| --- | --- | --- |
| Initializing (single-step) | `String[] arr = {"One", "Two", "Three"};` | `ArrayList<String> arrList = new ArrayList(Arrays.asList("One", "Two", "Three"));` |
| Initializing (multi-step) | `String[] arr = new String[3];` | `ArrayList<String> arrList = new ArrayList();` |
| Getting the number of elements | `arr.length;` | `arrList.size();` |
| Getting the element at index 0 |`arr[0];` | `arrList.get(0);` |
| Checking whether `"Seven"` is one of the elements | No built-in method. | `arrList.contains("Seven");` |
| Adding the element `"Five"` to the end | N/A | `arrList.add("Five");` |
| Adding the element `"Four"` to index 3, and shifting elements behind it forwards one index | N/A | `arrList.add(3, "Four");` |
| Getting the index of the first occurrence of `"Three"` | No built-in method. | `arrList.indexOf("Three");` |
| Getting the index of the last occurrence of `"Three"` | No built-in method. | `arrList.lastIndexOf("One");` |
| Removing all the elements | N/A | `arrList.clear();` |
| Printing all the elements	| `System.out.println(Arrays.toString(arr));` | `System.out.println(arrList);` |

Note: You need to import `java.util.ArrayList` or `java.util.*` in order for these `ArrayList` methods to work.

Java also has a class called `List`, which is similar to `ArrayList`. You won't be required to use `List` in this course, but you may use it if you feel that it would be useful.

   
> Exercise 9-3
>    
> Play around with this [Attendance](../Java_Programs/Attendance.zip) program. It is a GUI that modifies an array list based on user input.
 
