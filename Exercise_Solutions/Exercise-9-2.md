### Exercise 9-2 Solutions

Play around with regular expressions in Google Docs.

Open any of your documents (preferably one with a lot of words), open Find and Replace, click the checkbox beside "Match using regular expressions", and see what happens when you put the following regular expressions in the Find box.

1. `(a|i)(n|t)`

Matches all occurrences of `an`, `at`, `in`, and `it`. They might be part of a longer word. Not case-sensitive.


2. `T[^ ]e`

Matches all words that begin with `t` and end with an `e`. Not case-sensitive.


3. `[aeiou]t`

Matches all occurrences of `at`, `et`, `it`, `ot`, and `ut`. They might be part of a longer word. Not case-sensitive.


4. `[^aeiou]p`

Matches all occurrences of `p` unless there is a preceding `a`, `e`, `i`, `o`, or `u`. They might be part of a longer word. Not case-sensitive.


5. `e+`

Matches all occurrences of `e`, `ee`, `eee`, etc. Not case-sensitive.
