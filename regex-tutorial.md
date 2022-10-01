# Regex-Tutorial
A regualar expresstion is a sequence of characters that represents a search pattern within text. They help match, find, and in general manage text.

## Summary
Emails are one of the most common form of communication amongst any platform. As an developer, it is important to verify that an user input is a valid email address
In this tutorial, we will be demonstrating regular expression for emails using: 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.

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

### Anchors
In regex, anchors are used to assert the current position in the string matches a well-determined location. In the regex code above, ^ anchor symbolizes the beginning of the text and $ anchor symbolizes the end of the text.
/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/
as you can see above, it begins with ^ and ends with $

### Quantifiers
In regex, quantifiers elaborate how many instances of a character, or group must be presented in the input for a match to be found. In the regex code above, + is a greedy quantifer that there is another sequence to be matched and {2,6} tells us that the input should be a minimum of 2 characters and a maximum of 6 characters.
/^([a-z0-9_\.-]+)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/
the relevent parts of the regex are highlighted above

### OR Operator
In regex, an OR operator is declared where it starts with the `#` and following that either: 

`[a-f0-9]{6}` which will match a 6 character long string that contains a combination of a-f letters and 0-9 numbers. 

`|` OR Operator

`[a-f0-9]{3}` it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers. 

### Character Classes
In regex, character class is a set of characters enclosed within square bracket. In the regex code above, `\d` is a shorthand character for [0-9] that matches any character that is a digit. As shown below:
/^([a-z0-9_\.-]+)@([`\d`a-z\.-]+)\.([a-z\.]{2,6})$/

### Flags
In regex, a flag is typically used in this form : `/regex/`
It starts with the slashes inidcating the beginning and end, 
g: stands for global which will match all instances with the matching guidelines
m: stands for multilines which will search by line rather than the whole string
i: stands for insensitive and will make the expression case-sensitive so caps letters and nocaps letters do not stop you from matching

### Grouping and Capturing
There are three groups in the regex code above. 
 Group #1: `[a-z0-9_\.-]` is used for the username of the email account. 
 Group #2: `[\da-z\.-]` is used to capture the domain name/email service. 
 Group #3: `[a-z\.]` is used to capture the domain extension. 
 /^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

### Bracket Expressions
In regex, bracket expression is a list of characters enclose by `[]`. Much like the grouping and capturing section, there are three bracket expressions.
/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/
1: `[a-z0-9_\.-]` - includes case sensitive characters from a-z, numbers from 0-9 an underscore, periods and hyphens.

2: `[\da-z\.-]` - includes all digits, case sensitive characters from a-z, periods and hyphens
3: `[a-z\.]` - includes case sensitive characters from a-z and periods.

### Greedy and Lazy Match
In regex, 'Greedy Match' means that it will match the longest possible string while a 'Lazy Match' will do the shortest. In the code above, `+` would be used for a greedy search. If `>` is added to `+`, the mode would switch from greedy to lazy.
/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]{2,6})$/

### Boundaries
While in a string it will be with specific words. But are not used in the snippet.

### Back-references
Back-references are not used in the snippet

### Look-ahead and Look-behind
If using either of these then they have to match in specific ourders, but its not in the snippet

## Author

Created by Oliver Dirker and I am a full-stack web developer.
githhub link to profile: https://github.com/olliedirker