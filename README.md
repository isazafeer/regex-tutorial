# Regular Expressions

Regular expressions are often referred to as regex; they usually refer to a distinct string consisting of various characters that are used as query tools and validators in code bases and traditional documents.

## Summary

This tutorial will be covering the regular expression used for matching and validating an email:

`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

To match and validate an email, the regular expression shown above can also be used as a string inside a code base. For example, if users fill out certain forms that require a valid email address, the user won't be able to continue until they enter an certain number of characters followed by an @ symbol, followed by a domain name such as google, outlook, or yahoo, and the domain system name, such as '.com' or '.co.uk'. In this example, the domain system name must be between 2 and 6 characters long, so the domain system name could be '.com', '.co.uk', or '.net'.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

The regex components that define this expression are anchors, quantifiers, character classes, single character matches, brackets, grouping constructs and meta escape characters.

Using the example above:

* `^` and `$` are the anchors
* `+` and `{2, 6}` are the two quantifiers
* `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` represents the character classes
* `_`, `\.`, `-` represents the single character matches
* `()` represents utilizing grouping and capturing
* `\d` represents the meta escape characters utilised
* `[]` outlines the bracket expression

### Anchors

Anchors in regex mark the beginning and the end points of an expression. Here, the `^` marks the beginning and the `$` marks the end of the expression.

### Quantifiers

Quantifiers are meta characters that adjust the preceding character in a regular expression pattern by indicating the number of matches to be made in a row. Quantifiers also allow a user to specifiy how many characters or character classes can be matched.

* `+` matches one or more characters
* `{min, max}` allows a user to specify a numerical quantifier range. For example, in the expression above, `{2, 6}` indicates a range of characters for the domain system name.

### Grouping Constructs

Grouping constructs are identfied by `()`; this creates a sub expression and is able to class multiple characters as one. In the example above, the brackets are used 3 times to group a range of characters together, indicating the characters that can be used in each section of an email.

### Bracket Expressions

`[]`'s are used to create a character group to represent a single character. In the example, bracket expression is used to seperate multiple charcter classes.\

- - `[a-z0-9_\.-]` is from the example; this can be matched to any lower case character between 'a' and 'z', along with a digit from 0 - 9, with an underscore, period and dash.

### Character Classes

Character classes in a regex are attributes that allow a user to define a specific character or sets of them; they can be used in search patterns.

Using the example, the character classes are:

* `[a-z0-9_\.-]` 
- - `a-z` matches single characters from 'a' to 'z' (case sensitive).
- - `0-9` matches single characters from '0' to '9' (case sensitive).

* `[\da-z\.-]`
- - `d` matches any digit from 0 - 9.
- - `a-z` matches single characters from 'a' to 'z' (case sensitive).

* `[a-z\.]`
- - `a-z` matches single characters from 'a' to 'z' (case sensitive).

### The OR Operator

This specific regex example does not contain any OR operators; however, OR operators are usually identified as `|`.

### Flags

Flags in regular expressions are used to modify the way that an expression behaves; for example, it could be case sensitive.

In JavaScript, there are six different types of flags; 

* g - looks for all matches
* i - case sensitivity
* u - enables Unicode support
* s - enables "dotall" mode which allows a period to match a newline character
* m - multi-line mode
* y - "sticky" mode

### Character Escapes

Character escapes in regex usally represent a character that can not be represented in its literal form. Usually, a `/` is used to wrap a pattern together, but with character escapes, it is slightly different. Instead of a forward slash, they use a `\` (back slash), mainly because it is commonly used to escape a single character that would be interpreted literally.

## Author

Hi! Thank you for taking the time to read through this tutorial! 

My name is Isa Zafeer and I currently participate in a Coding Bootcamp, which will hopefully allow me to begin my career as a Full Stack Developer. When I'm not focusing on coding for homework or personal projects, I spend my time flying drones (I have a license) and 100% completing games. I'm a little bit of a... trophy hunter ;)

[Link to Github](https://github.com/isazafeer)
[Link to Gist](https://gist.github.com/isazafeer/2d2e3257a10f6356621dc997ac6599fe)
