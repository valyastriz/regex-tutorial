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

- **Example**: `/^hello/`  
This regex matches the word "hello" **only** if it appears at the **beginning** of the string (because of the `^`).

- **Example**: `/world$/`  
This regex matches the word "world" **only** if it appears at the **end** of the string (because of the `$`).

---

## Quantifiers

Quantifiers define how many times a character or pattern should appear in the text to make a match.

- **Example**: `/a{3}/`  
This matches exactly **three** consecutive "a" characters (e.g., "aaa" in "baaa").

- **Example**: `/a+/`  
This matches **one or more** "a" characters (e.g., "a", "aa", or "aaa").

---

## Grouping Constructs

Grouping combines parts of a pattern together, often for repeating, capturing, or applying conditions to them.

- **Example**: `/(abc)+/`  
This matches one or more instances of "abc" together (e.g., "abc", "abcabc").

- **Example**: `/(\d{3})-(\d{4})/`  
This matches a three-digit number followed by a hyphen and a four-digit number (e.g., "123-4567"), capturing both parts in separate groups.

---

## Bracket Expressions

Bracket expressions match any one of the characters inside the brackets.

- **Example**: `/[aeiou]/`  
This matches any **single vowel** (a, e, i, o, or u) in a string.

- **Example**: `/[A-Z]/`  
This matches any **uppercase letter** from A to Z.

---

## Character Classes

Character classes represent groups of characters, like all digits or all letters.

- **Example**: `/\d/`  
This matches any **single digit** (equivalent to `[0-9]`).

- **Example**: `/\w/`  
This matches any **word character**, including letters, digits, and underscores (equivalent to `[A-Za-z0-9_]`).

---

## The OR Operator

The `|` symbol allows you to match one pattern or another, like an "either-or" option.

- **Example**: `/cat|dog/`  
This matches **either** "cat" **or** "dog" in the string.

- **Example**: `/grape|orange|apple/`  
This matches **any of the words** "grape", "orange", or "apple" in a string.

---

## Flags

Flags modify how the regex works, like making it case-insensitive.

- **Example**: `/hello/i`  
This matches the word "hello" in a **case-insensitive** way, so it will match "Hello", "HELLO", etc. because of the `i` flag.

- **Example**: `/world/m`  
This enables the **multi-line mode**, allowing `^` and `$` to match at the beginning and end of each line in multi-line text.

---

## Character Escapes

Escapes are used to match special characters or predefined patterns, like digits or spaces.

- **Example**: `/\./`  
This matches a **literal period** character `.` in a string, rather than treating it as a wildcard for any character.

- **Example**: `/\d{2}-\d{2}-\d{4}/`  
This matches a date in the format "dd-mm-yyyy", using `\d` to match digits and `-` as a **literal hyphen**.

## Author

Written by Valentina Strizheus, a developer with an interest in regex and pattern matching. Find more of my work by visting [My Portfolio](https://valyastriz.github.io/Valya-Strizheus-Portfolio/)
