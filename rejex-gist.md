# HEX Value Regex

Regular expressions, or regex, are a series of characters which act as a key to help in searching texts for matching expressions. Regular expressions help us effectively search for phone numbers, emails addresses, street addresses, tracking ids, or any other pattern-base set of characters among large swaths of data.

## Summary

For this gist I will be looking at the regex for HEX values, which are used to identifying and displaying colors online. Additionally, I will be explaining what both the literal and meta characters in this regex represent and what their usages in searching HEX values. HEX values are represented with the # symbol and then either six or three characters, which use a mixture of numbers (all numbers 0-9) and letters (the letters a-f) in order to delineate the value of red, blue, and green hues within the color. For example, the HEX value for a light purple is #C6A1CF, and the code for dark green would be #006E33. The regex for HEX values is:
``` 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/.
``` 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
Anchors are meta characters used to match the position of the string. 

The symbols `^` and `$` are anchors for each side of the expression, where `^a` searches for strings which begin with `a` and `b$` searches for strings which end with `b`. In the case of our HEX value regex, we can see this in the beginning, where `^#` makes sure that the character string being selected begins with a `#`, and the `([a-f0-9]{6}|[a-f0-9]{3})$` makes sure that the string ends with a letter from a-f or a number from 0-9.

### Quantifiers
Quantifiers are used to specify how many times a certain pattern within the string must match the regex. 

For example, this regex uses `?` and `{n}`. Here, at the beginning of the regex, `^#?` the `?` works to indicate that the string must match the `#` at least one time. Additionally, inside the regex we see `{n}` employed with `n = 3` and `n = 6` where `([a-f0-9]{6}|[a-f0-9]{3})`. This works to ensure that the instances match n times, so that the HEX value is either 6 characters or 3 characters exactly.

### OR Operator
OR operators, `|`, are used so that the regex will match with two different types of strings. 

In our case, the OR operator splits our regex `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`into two sections: `[a-f0-9]{6}` and `[a-f0-9]{3})`. This makes it so expressions with either 6 characters or 3 characters can match the regex. 6 characters and 3 character strings are both accepted formats for HEX values.

### Character Classes
Character classes are used to identify and match one of the characters within the brackets to the characters being searched for. 

In our example of HEX values, `[a-f0-9]` is a character class, containing the requirements to match with any letter a-f and number 0-9. It is important to note here that character classes only match with a single character at time, which is why the quantifier (which is previously defined above) `{n}` is significant, as it tells it to run the search n times. In our case, the `{6}` and `{3}` each tell the regex to search either 6 or 3 times. 

### Grouping and Capturing
Grouping and capturing refers to the use of parentheses so that multiple regex components can be grouped together and the same function can be applied to each element.

For the HEX value regex, we see grouping and capturing in the parentheses which enclose our character classes: `([a-f0-9]{6}|[a-f0-9]{3})`. The function being applied is the `^#?` quantifier which ensures that each potential character string must being with a #.

### Bracket Expressions
Bracket expressions are the characters encased in the brackets of character classes. 

In this case, the bracket expressions are alphanumeric charecters. We see this in the `a-f0-9` sections of our regex.

## Author
To visit my profile, click [here](https://github.com/anniech1)!
