## Searching Arrays

### How Humans Search

How fast can you find the word "panda" in this grid? Don't use CTRL-F or ⌘-F!

| cat | goose | dog | lion | bear | snake | rabbit |
| --- | --- | --- | --- | --- | --- | --- |
| tiger | deer | fox | elephant | monkey | fish | pig |
| kangaroo | donkey | hyena | chinchilla | alpaca | capybara | horse |
| dolphin | swan | rhinoceros | cow | toad | duck | moose |
| turtle | hamster | otter | giraffe | zebra | penguin | leopard |
| frog | llama | goat | eagle | panda | raccoon | shark |
| squirrel | bat | sheep | groundhog | chipmunk | aardvark | camel |
 

Now, try finding the word "llama" in this grid. Again, don't use CTRL-F or ⌘-F!

| aardvark | chinchilla | duck | goat | leopard | penguin | snake |
| --- | --- | --- | --- | --- | --- | --- |
| alpaca | chipmunk | eagle | goose | lion | pig | squirrel |
| bat | cow | elephant | groundhog | llama | rabbit | swan |
| bear | deer | fish | hamster | monkey | raccoon | tiger |
| camel | dog | fox | horse | moose | rhinoceros | toad |
| capybara  | dolphin | frog | hyena | otter | shark | turtle |
| cat | donkey | giraffe | kangaroo | panda | sheep | zebra |
  

How were your strategies different for an unsorted grid versus a sorted (i.e. alphabetical) grid?

  
When humans look through an unsorted grid to look for a specific item, they tend to look in a logical order (i.e. starting in one corner and going across or up/down). Computers behave similarly when searching through an unsorted array in order to find a specific item. It starts from one end and continues in order until it finds the item.

When humans look through a sorted grid to look for a specific item, they tend to look for clusters of similar items (e.g. words that begin with the same letter), then go from there. Computers cannot do this, since they can only check one item at a time.

 
### How Computers Search

So, how would a computer efficiently search through a sorted array in order to find an item as fast as possible?

~The following grid has 49 words in alphabetical order (the first 7 are in the far left column). The text is white so that you cannot see them. (Spoiler tags aren't built into D2L.) How many words did you check until you found "sushi"? Check one word at a time by highlighting the cells in any order you wish.~


| same | sequence | shop | since | sloth | sock | stump |
| --- | --- | --- | --- | --- | --- | --- |
| scandal | shade | shore | sine | small | socket | summer |
| scarf | shall | show | sink | smash | soft | sushi |
| science | shame | shuck | sip | snack | sort | swamp |
| seat | shape | sigma | sit | snake | soup | swat |
| secant | sharp | sign | site | soap | squid | swish |
| sector | shoe | signal | slither | soccer | store | switch |

Note: Markdown does not support white text, so this exercise cannot be done in this format.

A computer would use an algorithm called binary searching to search for an item in a sorted array. It would check the middle item, and if it isn't the item it's looking for, it would make a binary decision: keep checking in the first half or keep checking in the second half. It would then check the middle item of the "half" it chose, and continue this process until it finds the item. This is the most efficient way that a computer can search for an item in a sorted array.

~Try a binary search on this grid with white text. How many words did you check until you found "purple"? If the algorithm is performed correctly, it should take no more than 6 guesses to find any given word (or determine that it isn't there) in array of 64 item.~


| amaranth | blue | cerulean | gold | lilac | orchid | raspberry | silver |
| --- | --- | --- | --- | --- | --- | --- |  --- |
| amber | blush | coffee | grey | lime | peach | red | tan |
| amethyst | bronze | copper | green | magenta | pear | rose | teal |
| apricot | brown | coral | indigo | maroon | periwinkle | ruby | turquoise |
| aquamarine | burgundy | crimson | ivory | mauve | pink | salmon | violet |
| azure | byzantium | cyan | jade | ocher | plum | sangria | viridian |
| beige | carmine | emerald | lavender | olive | puce | sapphire | white |
| black | cerise | erin | lemon | orange | purple | scarlet | yellow |

Note: Markdown does not support white text, so this exercise cannot be done in this format.
 
 

### Binary Search Algorithm

There are two common approaches to program a binary search algorithm.

**Approach 1: Iteration**
* Keep track of a lower bound and an upper bound for the index of the item in the array.
* If the lower bound is equal to the upper bound, the item is either at that index, or not in the array.
* In a loop, keep checking the middle item (half-way between the lower and upper bound).
  * If the middle item isn't what you're looking for, update the lower bound or upper bound depending on whether the item should appear before or after that middle item.
  * If the middle item is what you're looking for, you've found it!
 

**Approach 2: Recursion**

* If the array is empty, the item is not in the array.
* Check the middle item in the array. 
  * If the middle item isn't what you're looking for, repeat the entire process with either the first half of the array, or the second half depending on whether the item should appear before or after that middle item.
  * If the middle item is what you're looking for, you've found it!


> Exercise 11-1
> 
> Download and open the [Binary Search](../Java_Programs/BinarySearch.zip) project. Fill in the missing code in both methods. Only modify the commented areas.
> 
> Download solutions [here](../Java_Programs/BinarySearchSolution.zip.
