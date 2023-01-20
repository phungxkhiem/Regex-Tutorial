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