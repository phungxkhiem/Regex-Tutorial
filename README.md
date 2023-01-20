Regex Tutorial HTML
---
For this tutorial is specific to utilizing Regular Expressions (Regex) for matching an HTML tag. Implementation of a Regex in this way is a narrow pattern search. The following tutorial will help demonstrate the usage of an HTML Tag Regex search.

Summary
---
When a Regex or regular expression is used, it is done by identifying a pattern used in string-search based algorithms through a function known as FIND or FIND AND REPLACE.

The example of code for an HTML Tag search is as follows:

/^<([a-z]+)([^<]+)(?:>(.)</\1>|\s+/>)$/

You will need to have a working knowledge of what an HTML tag utilizes to understand this tutorial. Therefore, as a refresher, please note that an HTML tag contains < and > as an opening and closing "tag". You may have seen in previously viewed source code for a webpage the following examples: ,

,
, and so forth.
For every open tag, a closing tag must follow in order to contain the code within or else it will not be properly run. HTML tags are not always quite as simple as the prior example and can include various specific parts through which, when run, can deploy unique tasks. Consider the following:

