# Regex 101

I don't know a lot about regex.  I don't assume that many people know about how regex is.  Regex can be very useful.

https://regex101.com is your friend.

A lot of Regex tutorials or even makeshift Regex guides kind of miss the mark.

Here are some basics

Matching Characters:

    . (dot): Matches any single character except newline.
    [a-z]: Matches any lowercase letter.
    [A-Z]: Matches any uppercase letter.
    [0-9]: Matches any digit.
    \w (word character): Matches any alphanumeric character (a-z, A-Z, 0-9, and underscore).
    \s (whitespace): Matches any whitespace character (space, tab, newline).

Quantifiers:

    *: Matches zero or more of the preceding element.
    +: Matches one or more of the preceding element.
    ?: Matches zero or one of the preceding element.
    {n}: Matches exactly n occurrences of the preceding element.
    {m,n}: Matches between m and n occurrences of the preceding element.

Anchors:

    ^: Matches the beginning of the string.
    $: Matches the end of the string.

Grouping:

    (): Groups characters for repeated matching or capturing.

Other Symbols:

    \d: Matches any digit (equivalent to [0-9]).
    \D: Matches any non-digit (opposite of \d).
    \b: Matches a word boundary (beginning or end of a word).
    \: Escapes the special meaning of a following character.