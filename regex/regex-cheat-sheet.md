# RegEx Overview
A regex, or regular expression, is a special text string for describing a search pattern.

## Character classes
* `.` any character except new line
* `\w \d \s` word, digit, whitespace
* `\W \D \S` not word, digit, whitespace
* `[abc]` any of a, b, or c
* `[^abc]` not a, b, or c
* `[a-g]` character between a and g

## Anchors
* `^abc$` start/end of the string
* `\b \B` word, not-word boundary

## Escaped characters
* `\. \* \\` escaped special characters
* `\t \n \r` tab, linefeed, carriage return
* `\u00A9` unicode escaped copyright symbol

## Groups & Lookaround
* `(abc)` capture group
* `\1` backreference to group `#1`
* `(?:abc)` non-capturing group
* `(?=abc)` positive lookahead
* `(?!abc)` negative lookahead

## Quantifiers & Alternation
* `a* a+ a?` 0 or more, 1 or more, 0 or 1
* `a{7} a{3,}` exactly seven, three or more
* `a{1,4}` between one and four
* `a+? a{3,}?` match as few as possible
* `ab|cd` match ab or cd
