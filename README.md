# Regex Tutorial

## Description
This tutorial will provide multiple in depth explanations on using Regular Expressions in JavaScript to match URLs. It will give a brief overview for each component, as well as provide a couple of examples to better your understanding.


## Table Of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracker-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


## Anchors{#anchors}
Anchors refer to special charcters or a sequence of characters. They are used to specify where in the string a match should occur.

1. Start Anchor ^: This asserts that the pattern must match the start of the string.
2. End Anchor $: This asserts that the pattern must match the end of the string.

Example of a regex pattern that can be used to match a URL:

```javascript 
const urlRegex = /^(https?|ftp):\/\/[^\s/$.?#].[^\s]*$/; 

## Quantifiers{#quantifiers}
Quantifiers are used to specify how many times a pattern should match. They are placed after a character, character class, or group.

- *: 0 or more times.
- +: 1 or more times.
- ?: 0 or 1 time.
- {n}: Exactly N times.
- {n,}: At least n times.
- {n,m}: Between n and m times.

Example of a quantifier in a regex pattern:
```javascript
const digitRegex = /\d{3}/;

## Grouping Constructs{#grouping-constructs}
Grouping constructs in regex are used to group together one or more characters and treat them as a single unit within the expression. They are enclosed with parentheses.

- (...): Capturing group
- (?:...): Non-capturing group

Example of using grouping constructs in a regex pattern: 

const dateRegex = /(\d{2})-(\d{2})-(\d{4})/;
Explanation of the regex pattern:

(\d{2}): Grouping construct that matches exactly 2 digits.
-: Matches the hyphen character literally.
(\d{2}): Grouping construct that matches exactly 2 digits.
-: Matches the hyphen character literally.
(\d{4}): Grouping construct that matches exactly 4 digits.

## Bracket Expressions {#bracket-expressions}
Bracket expressions allow you to specify a set of characters that can match a single character at that position in the input string. They are denoted by square brackets, and any character enclosed within these brackets will become a part of the allowed set.

Example of using bracket expressions in a regex pattern:
const vowelRegex = /[aeiou]/;
Explanation of the regex pattern:

[aeiou]: Bracket expression that matches any single character that is either 'a', 'e', 'i', 'o', or 'u'.


## Character Classes{#character-classes}
Character classes allow you to match a single character from a specific set of characters. With the use of character classes, you can simplify and shorten regex patterns, making them easier to understand.

Example of using character classes in a regex pattern:

const digitRegex = /[0-9]/;
Explanation of the regex pattern:

[0-9]: Character class that matches any single digit character from '0' to '9'.


## The OR Operator{#the-or-operator}
The 'or' operator is represented by the vertical bar | character. It allows you to specift multiple alternatives for a pattern to match.

Example of using the 'or' | operator in a regex pattern:

const fruitRegex = /apple|banana|orange/;
Explanation of the regex pattern:

apple|banana|orange: The "or" operator | allows the regex to match either "apple", "banana", or "orange".

## Flags{#flags}
Flags are optional parameters that modify how the regex pattern is interpreted or applied during matching. They are modifiers that affect the behavior of regular expressions by enabling or disabling certain features and are appended to the end of the regex pattern.

Some common flags used in JavaScript regex include: 

i (ignore case): This flag makes the regex pattern case-insensitive, allowing it to match both uppercase and lowercase characters interchangeably.

Example: /hello/i will match "hello", "Hello", "HELLO", etc.
g (global search): This flag enables the regex pattern to find all matches in a string, rather than stopping after the first match.

Example: /apple/g will find all occurrences of "apple" in a string.
m (multiline): This flag changes the behavior of ^ and $ anchors to match the start and end of each line within a multi-line string.

Example: /^start/m will match "start" at the beginning of each line.

## Character Escapes{character-escapes}
Character escapes are special sequences that represent characters with special meanings or characters that are difficult to represent directly. Character escapes are an essential aspect of regex, allowing for accurate pattern matching.

Some common character escapes in regex include:

\d - Matches any digit character (equivalent to [0-9]).
\w - Matches any word character (alphanumeric character or underscore).
\s - Matches any whitespace character (space, tab, newline).
\n - Matches a newline character.
\t - Matches a tab character.
\. - Matches a literal period (dot) character.

## Author
Written by Selena Pixton
- Github: [SelenaPix's GitHub Profile](https://github.com/selenapix)
- Repo: [SelenaPix's Regex Repo](https://github.com/selenapix/regex-repo)
- Gist: [SelenaPix's Gist](https://gist.github.com/selenapix/f7d608cc4c67fe3abc3cb627ac2a9018)
