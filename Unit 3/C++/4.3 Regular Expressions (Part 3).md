# [Link to video.](https://www.youtube.com/watch?v=BGTm1fVUatM&list=PLVD25niNi0Blds9kjuux3nj9N9n5nBpMr)

### Regular Expressions

Suppose we have a long string and we want to extract every substring that follows a particular pattern. We can use a string regex iterator to go through the string to check for all possible matches.

```cpp
regex phoneRegex("\\([0-9]{3}\\) [0-9]{3}\\-[0-9]{4}"); // this is the pattern for phone numbers that looks like this: (___) ___-___

string phoneNumbers = "(519) 885-4620 ~~ (519) 888-9749"; // there are two phone numbers in here we want to extract

auto phoneBegin = sregex_iterator(phoneNumbers.begin(), phoneNumbers.end(), phoneRegex);
auto phoneEnd = sregex_iterator(); // once phoneBegin iterates through the entire string, it will be equivalent to the default sregex iterator

for (auto iter = phoneBegin; iter != phoneEnd; iter++) { // this iterator will go through the string to check for matches
  smatch match = *iter; // sets match to the string the iterator is pointing at (we'll see why the * is necessary later this unit)
  cout << match.str() << endl; // this will print the substring if it matches the pattern
}
```
