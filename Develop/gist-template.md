# Regular Expressions

Regular Expressions or regex for short, are patterns used to match characters in strings.

## Summary

We will be exploring a regex that is used to identify if a particular string has the characteristics of an email address.
Code snippet is shown below

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Bracket Expressions](#grouping-and-bracket-expressions)
- [Explanation](#explanation)

## Regex Components

### Anchors

Anchors do not match any characters, rather they match a position before/after characters/

```^``` This is called the caret anchor. It matches the beginning of text
```$``` This is called the dollar anchor. It matches the end of text

In our email regex we can see that there is a caret anchor at the start

### Quantifiers

Quantifiers match the number of instances of a character. 

Exact count quantifiers:

```{n}``` will match a character that appears n times

Range quantifiers:

```{n,m}``` will match a character that appears between n to m times


### Character Classes

Character classes allow matching from a certain character set.
```\d``` specifies a digit class
```.``` the dot class matches any character except a newline

Escape characters may be added by a backslash

```\.``` adds a period to the search pattern


### Grouping and Bracket Expressions

Sets allow searching for any character in a set
```[abc]``` will match any of the three characters ```'a'```, ```'b'```, ```'c'```

Ranges allow matching any character that appears in a range
```[a-z]``` matches any character between ```a``` and ```z```

The ```+``` sign:

A regex followed by a ```+``` sign matches one or more occurences of the one-character regex

If an expression is enclosed in paranthesis, the editor treats it as one expression and applies signs to the whole expression

```a+b``` matches ```ab``` but not `b`

### Explanation

```^``` creates a start anchor

```/^([a-z0-9_\.-]+)``` Expression must match lowercase letters between a-z, numbers between 0-9, underscore, periods or hyphens

This is followed by an @ sign

```([\da-z\.-]+)``` domain must be digits, letters between a-z, periods or hyphens

This is followed by a period

```([a-z\.]{2,6})``` Matches a group of letters or periods 2-6 characters long.

This is followed by ```$``` which is the end anchor



## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
