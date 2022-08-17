# HEX Value Regex

Regular expressions, or regex, are a series of characters which act as a key to help us search texts for matching expressions. They helps us effectively search for phone numbers, emails addresses, street addresses, tracking ids, or any other pattern-base set of characters in large swaths of text.

## Summary

For this gist I will be looking at the regex for searching HEX codes, which are used in identifying and displaying colors. HEX codes are represented with the # symbol and then either six or three characters, which use a mixture of numbers (all numbers 0-9) and letters (the letters a-f) in order to delineate the value of red, blue, and green hues within the color. For example, the HEX value for a light purple would be #C6A1CF, or the code for a dark green would be #006E33. The regex for HEX values is:
``` 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/.
``` 
I will be explaining what the both literal and meta characters in this regex represent and what their usages are when a user is searching for HEX codes.

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
Anchors are meta characters used to match the position of the string. 

The symbols `^` and `$` are anchors for each side of the expression, where `^a` searches for strings which begin with `a` and `b$` searches for strings which end with `b`. In the case of our HEX value regex, we can see this in the begining, where `^#` makes sure that the character string being selected begins with a `#`, and the `([a-f0-9]{6}|[a-f0-9]{3})$` makes sure that the string ends with a letter from a-f or a number from 0-9.

### Quantifiers
Quantifiers are used to specify how many times a certain pattern within the string must match the regex. 

For example, this regex uses `?` and `{n}`. Here, at the begining of the regex, `^#?` the `?` works to indicate that the string must match the `#` at least one time. Additionally, inside the regex we see `{n}` employed with `n = 3` and `n = 6` where `([a-f0-9]{6}|[a-f0-9]{3})`. This works to ensure that the instances match n times, so that the HEX code is either 6 characters or 3 characters exactly.

### OR Operator
OR operators, `|`, are used so that the regex will match with two different types of strings. 

In our case, the OR operator splits our regex into two sections, `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`, into `[a-f0-9]{6}` and `[a-f0-9]{3})`. This makes it so expressions with either 6 characters or 3 characters can match the regex, as these are both accepted formats for HEX codes.

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

To visit my profile, click [here](https://github.com/anniech1)!
