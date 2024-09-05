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

### Anchors
Anchors are used to match a pattern at a specific position in the text, like the beginning or end of a line.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
