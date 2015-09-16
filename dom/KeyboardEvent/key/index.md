---
title: key
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary, examples, compatibility, standards, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/KeyboardEvent
    href: /dom/KeyboardEvent
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/KeyboardEvent/key

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/KeyboardEvent](/dom/KeyboardEvent)[dom/KeyboardEvent](/dom/KeyboardEvent)

## Syntax

``` js
var result = element.key;
element.key = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Key identifiers are strings that uniquely identify keyboard buttons, such as `Q`, `Home`, or `F2`. The string can be any of the following types:

-   Character string: A single character, such as a letter or symbol
-   Key name: A multicharacter string such as `Enter` or `Tab`
-   Unicode codepoint: "U+" followed by a hexadecimal character index

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Events Specification](http://go.microsoft.com/fwlink/p/?linkid=203756), Section 5.2.6
