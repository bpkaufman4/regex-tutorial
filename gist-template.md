# Email Matching Regex Tutorial

## Summary

In this file I will explain the components of an [email matching regular expression](https://gist.github.com/bpkaufman4/848d9ab00b1767199fb3b4ad16e71bca) and how it functions.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

The components of this particular regex are Anchors, quantifiers, character classes, and grouping and capturing.

### Anchors

An anchor in a regular expression is a charagter used to match a position before or after characters. For instance, in this regex the `^` character marks the beginning of the email address, and the `$` marks the end of it.

### Quantifiers

The `+` character is considered a wildcard meta-character. It represents the concept of one characters or more. It's function in this regular expression is to say that any number of characters can be present before `@`, between `@` and `.`, and after `.` because emails can varry in the number of characters in those locations. This tells the code that the regex is looking for any number of one or more characters, then the character `@`, then any number of one or more characters, then `.`, then any number of one or more characters.

### Character Classes

Character classes match the type of character the expression is looking for. This regex uses `\d` to mark where digits would be allowed. The `\` caracter alone indicates that within the character class, the `.` loses its meaning withing the regex and it is now searching for a literal `.` character. We also see a literal `@`, which is a has a literal character class, meaning it is matching that character if and only if that character is `@`.

### Grouping and Capturing

This regex uses `[]` to group character classes. For instance, `[a-z0-9_\.-]` is used to say that any of those character classes are allowed in this grouping. `()` is used to group what is inside and remember the match.

## Author

Brian Kaufman is a web-developer with a background in music and automotive mechanics. To visit his github click [here](https://github.com/bpkaufman4).
