# Regex Tutorial HTML
---
For this tutorial is specific to utilizing Regular Expressions (Regex) for matching an HTML tag. Implementation of a Regex in this way is a narrow pattern search. The following tutorial will help demonstrate the usage of an HTML Tag Regex search.

## Summary
---
When a Regex or regular expression is used, it is done by identifying a pattern used in string-search based algorithms through a function known as FIND or FIND AND REPLACE.

The example of code for an HTML Tag search is as follows:

/^<([a-z]+)([^<]+)(?:>(.)</\1>|\s+/>)$/

You will need to have a working knowledge of what an HTML tag utilizes to understand this tutorial. Therefore, as a refresher, please note that an HTML tag contains < and > as an opening and closing "tag". You may have seen in previously viewed source code for a webpage the following examples: ,

,
, and so forth.
For every open tag, a closing tag must follow in order to contain the code within or else it will not be properly run. HTML tags are not always quite as simple as the prior example and can include various specific parts through which, when run, can deploy unique tasks. Consider the following:

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Through the usage of anchors we define where the search parameters begin and end. Anything after ^ (caret) and before $ (dollar) are part of the search definition. The character immediately following a caret is identified by it's position within a search, as is the character preceding the dollar.

^abc123$

The caret, ^, identifies the beginning of our string where we have the algorithm set to match the position rather than the character. As with the dollar, $, it identifies the end of our search string within the algorithm.

For the HTML tag regex, we set up the pattern string search as /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/ which means we have the open and closing tags at the beginning and end of the string.
### Quantifiers
We use quantifiers in regex to determine where our preceding token string must be matched a pre-set number of times or more. A quantifier has the capacity of being greedy or lazy, which is further notated below:

+

this quantifier maintains that the search must match one or more of the characters set in the algorithm
characters placed to the left of the + are expected to match at least once
example: A+; the quantifier + is applied for a search for A
example: apples+ the quantifier + is ONLY applied to the s in apples rather than the entire word
*

this quantifier maintains that the search must match 0 or more times
?

this quantifier maintains that the search must match 0 or 1 times; it is considered optional
when implemented, it makes the preceding quantifier lazy, permitting it to match as few times as possible; whereas by default with our algorithm, quantifiers tend to gravitate towards matching as many characters as possible and are considered greedy as a result
{7,9}

the algorithm is set to force characters between seven and nine characters long
abc|cba

results in a match of abc OR cba only

### OR Operator
|
This operator acts like a Boolean OR. It causes a match of the expression before or after the | and can be utilized inside a group or on a whole expression. In terms of order, it causes the search-string to look for a match of either what precedes or follows after the |. In the example: <abc>|<cba> it is looking for either <abc> or <cba>.
### Character Classes
In order to search for match characters between a specific range of character, we create what is called "character classes".

Some example types:

\w This will match any word character (alphanumeric and underscored) such as [a-z0-9_], but will only match lowercase character without accent marks.

\W This matches any character that is not a word character (alphanumeric and underscored) such as [A-Za-z0-9_]

\d sets the search to match any digitized character such as 0-9

\D` sets the search for non-digitized characters

\p sets the match for a character in the specific unicode category

[A-Z] utilizing the hyphen between the two characters creates a range for the search criteria

' is a wildcard and will accept any input
### Flags
---
i ignores case

g is a modifier to perform a global match which finds all matches instead of stopping after the first match. For case-sensitive matches, combine g with the i modifier.

m is a multiline flag enabled to match the start and end of a line, rather than the start and end of a whole string. The anchors used at the beginning and end should reflect what we've learned previously: ^ and $.

s is a global search for whitespace characters within a string
### Grouping and Capturing
---
(abc){3} if we desired to group a selective pattern, we can introduce them between parentheses and include a numeric counter besides it. This example would search for the match of abcabcabc because the first group was denoted as (abc) and we included the need for it to repeat three times as {3}.
### Bracket Expressions
----
A regular expression surrounded by square brackets is considered a bracket expression meant to match a single character or collating element. When the first character is a circumflex ^ then the bracket expression is complemented. An example is [a-z] as a bracket expression.
### Greedy and Lazy Match
-----
Earlier, greedy and lazy matches were briefly remarked in Quantifiers.

A greedy quantifier tells the search algorithm to match as many instances of the pattern presented as possible. It is the longest possible string match.
### Boundaries
----
There are three separate positions to qualify as a word boundary:

before the initial character in the string, if the first character is a word character

after the last character in a string, if the last character is a word character

between two characters within the string, where one is a word character while the other is not a word character

### Back-references
Backreferences will match the same text previously matched by a capturing group. If you wish to match a pair of opening and closing HTML tags and the text in between, you can introduce it as follows:

<([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>

### Look-ahead and Look-behind
----
Also known as "lookaround", the Look-Ahead and Look-Behind are zero-length assertions. The main difference with it is that they actually match characters and gives up the match, returning only the result: match or no match. They are called "assertions" since they do not consume the characters in the string, but assert whether a match is possible or not.

## Author
---
phungxkhiem explained this tutorial - https://github.com/phungxkhiem/Regex-Tutorial