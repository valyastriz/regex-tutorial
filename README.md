# Lookaheads and Lookbehinds in Regular Expressions

Regular expressions (regex) are useful tools that help you search for patterns in text. Lookaheads and lookbehinds are advanced regex features that let you check if a pattern comes before or after another pattern, without including that extra pattern in the final match. These techniques help ensure a match is correct based on the surrounding text, but they don’t capture or include that surrounding text in the result.

## Summary

Lookaheads and lookbehinds allow you to match a pattern only if certain conditions are met, like if it’s followed or preceded by another pattern. However, these surrounding patterns aren’t part of the final match. For example, a positive lookahead checks if a pattern is followed by something specific, while a negative lookbehind checks if a pattern is not preceded by something.

Here’s a simple example: the regex below matches digits only if they are followed by “px” but doesn’t include “px” in the match itself:

```regex
\d(?=px)
```

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

## Anchors

Anchors are used to match a pattern at a specific position in the text, like the beginning or end of a line.

- **Example**: `/^**\d**(?=px)$/`  
In this regex, `^` is an anchor that asserts the match must be at the beginning of the string, and `$` asserts that it must be at the end.

## Quantifiers

Quantifiers define how many times a character or pattern should appear in the text to make a match.

- **Example**: `/^**\d+**(?=px)$/`  
Here, the `+` is a quantifier that specifies one or more digits must appear for a match.

## Grouping Constructs

Grouping combines parts of a pattern together, often for repeating, capturing, or applying conditions to them.

- **Example**: `/^**(\d+)(?=px)**$/`  
In this regex, the parentheses `(**)` are grouping constructs, capturing one or more digits.

## Bracket Expressions

Bracket expressions match any one of the characters inside the brackets.

- **Example**: `/^**[0-9]+**(?=px)$/`  
Here, `[0-9]` is a bracket expression that matches any digit between 0 and 9.

## Character Classes

Character classes represent groups of characters, like all digits or all letters.

- **Example**: `/^**\d+**(?=px)$/`  
The `\d` is a character class shorthand for any digit, equivalent to `[0-9]`.

## The OR Operator

The `|` symbol allows you to match one pattern or another, like an “either-or” option.

- **Example**: `/^**(\d|\w)+**(?=px)$/`  
The `|` is the OR operator, allowing the match to be either digits (`\d`) or word characters (`\w`).

## Flags

Flags modify how the regex works, like making it case-insensitive.

- **Example**: `/^(\d+)(?=px)$/i`  
The `i` is a flag that makes the regex case-insensitive. Although not needed here, it’s commonly used when case doesn’t matter.

## Character Escapes

Escapes are used to match special characters or predefined patterns, like digits or spaces.

- **Example**: `/^**\d**(?=\px)$/`  
The `\d` is a character escape used to match any digit (0-9).

## Author

Written by Valentina Strizheus, a developer with an interest in regex and pattern matching. Find more of my work by visting [My Portfolio](https://valyastriz.github.io/Valya-Strizheus-Portfolio/)
