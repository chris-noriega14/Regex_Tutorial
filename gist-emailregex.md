# Regex Expression for Email Validation

This document explains the functionality of a regular expression (regex). This tutorial will explain every part of the expression by breaking it down by each character. This regex is useful when validating emails using relational databases.

# Summary

The regular expression that we will be breaking down will be a regex that will validate email addresses. The full regex is displayed below:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

# Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

# Regex Components

Symbols inside the double forward-slashes (//) act as the body of the regex.
The first slash represents the beginning of the regex, and the second represents the end of the regex.

## Anchors
"^" - Anchors a match to the beginning of a line since it is used as the first character in this regex.

"$" - Matches the ending position of the string.

## Quantifiers
"+" - The plus sign matches at least one of the preceding token.
Two instances in this regex: 
[a-z0-9_\.-] 
and [a-z\.].

"{}" - Takes up to two integers ({2,6} in this regex). The expression matches the specified quantity of the token before it, in this case [a-z\.]. Top-level domain is 2-6 characters long. Examples include: .net, .com, .ca

## Grouping Constructs
"()" - Three instances: ([a-z0-9_\.-]+), ([\da-z\.-]+), and ([a-z\.]{2,6})

"()" - This expression groups multiple tokens together. This also creates a capture group. Capture groups are used for extracting substrings or for using a backreference.

## Bracket Expressions
Two instances: [a-z0-9_\.-] & [a-z\.].

[] - A bracket expression is a list of characters enclosed by brackets. The result matches any single character in the list.

## Character Classes
Character Classes for this regex include \d and .

\d - Matches any one digit character (0-9). 

. - Matches any character.

## The OR Operator
There are no OR operators ("|") in this regex. OR operators are used to match characters or expressions of either the left or right side of the operator.

## Flags
There are no flags in this regex; they are used to change the way a part of the expression is interpreted.

## Character Escapes
There are no character excapes in this regex. They are used to insert reserved, special, and unicode characters.

## Author
This concludes the tutorial for understanding the regex for validating email addresses. 
I am a full-stack developer with a passion for solving problems. You can view my GitHub at https://github.com/chris-noriega14.