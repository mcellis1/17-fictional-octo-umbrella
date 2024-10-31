# HexCode RegEx Tutorial

RegEx, or regular expressions, are a way to check if certain characters or values are contained within a word or phrase. This can be useful for things like validating email addresses, or checking to see if a password has at least one of a special character.

## Summary

The regex that I am going to be breaking down `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` is one that is designed to validate a hexadecimal code. 

A hex code is a pound sign followed by 6 numbers that coresponds to a unique color. Each color has a unique hex code, and hex codes can be used in coding to assign a unique color value.

## Table of Contents

- [Anchors](#anchors)
- [Character Classes](#character-classes)
- [OR Operator](#or-operator)
- [Quantifiers](#quantifiers)

## Regex Components

A regex is always encompassed by two backslashes. You can see the `/` at the beginning and the end. This is called a literal in code.

```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/```

### Anchors

The anchor tags denote where the regex will start looking and where it will stop looking. The `^` anchor goes at the beginning so that the regex knows to search for everything from the beginning of the phrase starting with this symbol. Since the `#` is located directly after the opening anchor, that means that the regex will only look for values or phrases that begin with a `#` symbol.

Likewise the `$` symbol denotes where the regex ends its search. Anything between these two parameters determines what the regex is looking for. If there were another symbol located after the parathesis, then that would mean the regex was looking for a specific character located at the end of the phrase, but there is nothing located after the closing parenthesis and the closing anchor.

### Character Classes

The bracketed expression `[a-f0-9]` means that the regex will look for any phrase that contains any of the alphabet between a to f and any number from 0 to 9. If the phrase has a character outside of this range, then the regex will ignore it.

### OR Operator

There are two phrases that the hex code regex is looking for. It can either look for a phrase that matches the conditions on the left side of the or operator, or match the conditions on the right side. This or operator is coded by wrapping both expressions in parenthesis `()` and then placing the vertical pipe character `|` in between the two phrases, either of whcih you wish to locate.

```(must meet either these conditions|or these)```

### Quantifiers

The first quantifier that the regex uses is the `?` that immediately follows the `#`. This quantifier says that the regex is either looking for one or zero phrases with this element. So our regex will look for phrases that begin with a pound sound, and also ones that do not, so long as they meet the other conditional requirements.

The curly brackets `{}` are what determine the quantity of characters that the regex is looking for. In our phrase, the regex is either looking for a phrase with `{6}` characters or one with `{3}` characters.

## Author

This gist was written by github user mcellis1![https://gist.github.com/mcellis1]
