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

the ^ is used to tell the regex that a string should start with the character following it (case sensitive) (brackets used if multiple starting characters are aloud) ^[a-z] must start in a letter from a to z

the $ is used to tell the regex that a string should end with the character before it ^^
[a-z]$ must end in a letter from a to z

### Quantifiers
Quantifiers set the limits of the string that your regex matches usually setting the minimun and maximum values the regex is searching for
(look at greedy and lazy match)
### OR Operator
OR Operators are mainly used in grouping constructs to make it so the search doesnt need to meet all of the requirements in the pattern 
(a|b|c):(x|y|z) (abc:xyz)

### Character Classes
Character Classes are used to define a set of characters inside of a regex

Some common Character Classes:

.—Matches any character except the newline character (\n) 

\d—Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9]. \d{2} grabs numerals which have 2 digits (00)

\w—Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_].

\s—Matches a single whitespace character, including tabs and line breaks \s{2} would grab any double spacing (  )

### Flags
Flags are used to define extra functionality/ limits of the regex and are placed outisde of the slash characters at the end, there are a total of 6 flags

3 of the most common flags are 

g—Global search: the regex should be tested against all possible matches in a string./^[a-c]{3,16}$/g (ht(acb)as)

i—Case-insensitive search: case should be ignored while attempting a match in a string /^[a-i]{3,16}$/g (aaFiaD)

m—Multi-line search: a multi-line input string should be treated as multiple lines

### Grouping and Capturing
grouping constructs are used to check multiple parts of a string by breaking the construct into sections (abc):(xyz) they have two functions, to capture or to not capture, and to not capture something you add a ? to the beginning of the expression inside the parentheses

### Bracket Expressions
Bracket Expressions are used to respresent a range of characters that we want to search for, they can be used by individualy typing out what you would like to search for or you can put a hyphen inbetween letters or numbers to search through them, they will grab upper or lower case letters you can also grab negative character groups by putting a  ^ at the beginning of the bracket to search for things that dont include those characters {a-c} (abc cab) {^a-c} 

### Greedy and Lazy Match
greedy matching means it will grab as many occurences of a specific pattern as possible

some of them are as follows

"*"  - Matches the pattern zero or more times [a-c]* grab all charcters (adsfnoasdgnsdv asdfads)

"+" - Matches the pattern one or more times [a-c]+ would grab all letters that are a to c (acbbbca)

? - Matches the pattern zero or one time [a-c]+[a-c]? grabs all characters a-c (abc acb a c b)
 
{} - Curly brackets can provide three different ways to set limits for a match:

    { n } — Matches the pattern exactly n number of times ^[a-z]{3} must be exactly three letters (adb)

    { n, } — Matches the pattern at least n number of times ^[a-z]{3,} must be the same or more than three letters (adqs) 

    { n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times\(\[a-z\]\+\) \\1 ^[a-z]{3,16} needs to be between 3 and 16 characters (saisdj)

lazy matching means it will grab as few occurences as possible, and to do this you put a ? after the quantifier

### Boundaries
Boundaries are usually a letter, digit, or underscore, they are used to create more constructs, such as \bcat\b would grab theres a black cat but not tomcat whereas \bcat would grab cat and catfish but not tomcat but cat\b would grab cat and tomcat but not catfish

### Back-references
Back-references are used to search for a previouslt matched group inside the same constructor and can be used like ([a-z]+) \1 (t t b b)

### Look-ahead and Look-behind
lookaround assertions matches characters ahead or behind of it but do not send the character, only gives you a match or no match. q(?=u) is a lookahead that searches for a q that is followed by a u but only returns a q. there are negative lookaheads aswell q(?!u) would returns any q that is not followed by a u. (?<=a)b is a lookbehind which would grab any b that is preceeded by an a, whereas (?<!a)b would return any b that is not preceeded by an a

### Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

^([a-z0-9_.-]+) ^ is an anchor and makes it start with  a-z 0-9 or . _ -  [a-z0-9_.-] is a character classes and checks the first part of the email address to make sure it has either a-z 0-9 or . _ -.  The + is a quantifier that specifies that there should be at least one character in this set

the @ matches the at symbol that separates the start from the domain name.

([\da-z.-]+) is a character classes this checks domain name, which includes the domain and any subdomains. [\da-z.-] matches any digit, lowercase letter, dot, or hyphen. The + quantifier specifies that there should be at least one 

.  This checks the period that separates the domain name from the top-level domain.

([a-z.]{2,6}) [a-z.] This checks the domain, can be lowercase letters and periods. {2,6} a quantifier which specifies that there should be between two and six characters.

$/ is an anchor that specifies that the string should end at this point.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

