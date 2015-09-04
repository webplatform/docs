---
title: tagName
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'summary, clean-up MSDN import'
uri: dom/HTMLElement/tagName

---
# tagName

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.tagName;
element.tagName = value;
```

## Examples

This example retrieves the tag name of an object that has the identifier specified in the prompt window.

    <SCRIPT>
    var idValue = window.prompt("Get the tag with this ID:");
    if (idValue != null) {
        alert(document.all[idValue].tagName)
    }
    </SCRIPT>

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

