# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

a regex is a sequence of characters that defines a search pattern for text

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
/^[a-z0-9_-]{3,16}$/
### Anchors
^ and $ are both anchors 

the ^ is used to tell the regex that a string should start with the character following it (case sensitive) (brackets used if multiple starting characters are aloud)

the $ is used to tell the regex that a string should end with the character before it ^^

### Quantifiers
Quantifiers set the limits of the string that your regex matches usually setting the minimun and maximum values the regex is searching for

### OR Operator
OR Operators are mainly used in grouping constructs to make it so the search doesnt need to meet all of the requirements in the pattern 
(a|b|c):(x|y|z) is how they can be used

### Character Classes
Character Classes are used to define a set of characters inside of a regex

Some common Character Classes:

.—Matches any character except the newline character (\n)

\d—Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

\w—Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_].

\s—Matches a single whitespace character, including tabs and line breaks

### Flags
Flags are used to define extra functionality/ limits of the regex and are placed outisde of the slash characters at the end, there are a total of 6 flags

3 of the most common flags are 

g—Global search: the regex should be tested against all possible matches in a string.

i—Case-insensitive search: case should be ignored while attempting a match in a string

m—Multi-line search: a multi-line input string should be treated as multiple lines

### Grouping and Capturing
grouping constructs are used to check multiple parts of a string by breaking the construct into sections (abc):(xyz) they have two functions, to capture or to not capture, and to not capture something you add a ? to the beginning of the expression inside the parentheses

### Bracket Expressions
Bracket Expressions are used to respresent a range of characters that we want to search for, they can be used by individualy typing out what you would like to search for or you can put a hyphen inbetween letters or numbers to search through them, they will grab upper or lower case letters you can also grab negative character groups by putting a  ^ at the beginning of the bracket to search for things that dont include those characters

### Greedy and Lazy Match
greedy matching means it will grab as many occurences of a specific pattern as possible

some of them are as follows

"*"  - Matches the pattern zero or more times

"+" - Matches the pattern one or more times

? - Matches the pattern zero or one time

{} - Curly brackets can provide three different ways to set limits for a match:

    { n } — Matches the pattern exactly n number of times

    { n, } — Matches the pattern at least n number of times

    { n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times

lazy matching means it will grab as few occurences as possible, and to do this you put a ? after the quantifier

### Boundaries
Boundaries are usually a letter, digit, or underscore, they are used to create more constructs, such as \bcat\b would grab theres a black cat but not tomcat whereas \bcat would grab cat and catfish but not tomcat but cat\b would grab cat and tomcat but not catfish

### Back-references
Back-references are used to search for a previouslt matched group inside the same constructor and can be used like ([a-z]+) \1

### Look-ahead and Look-behind
lookaround assertions matches characters ahead or behind of it but do not send the character, only gives you a match or no match. q(?=u) is a lookahead that searches for a q that is followed by a u but only returns a q. there are negative lookaheads aswell q(?!u) would returns any q that is not followed by a u. (?<=a)b is a lookbehind which would grab any b that is preceeded by an a, whereas (?<!a)b would return any b that is not preceeded by an a

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

