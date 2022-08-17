# HEX Value Regex

Regular expressions, or regex, are a series of characters which act as key to help us search text blocks for a matching pattern. They helps us effectively search for phone numbers, emails addresses, street addresses, tracking ids, or any other pattern-base set of characters in large swaths of text.

## Summary

For this gist I will be looking at the regex for searching HEX codes, which are used in identifying and displaying colors. HEX codes are represented with the # symbol and then either six or three characters, which use a mixture of numbers (all numbers 0-9) and letters (the letters a-f) in order to delineate the value of red, blue, and green hues within the color. The regex for HEX values is:
``` 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/.
``` 
I will be explaining what the literal and meta characters in this regex represent and what their usages are when a user is searching for HEX codes.

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


### Quantifiers

### OR Operator

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
