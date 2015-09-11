---
title: tagName
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/tagName

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var result = element.tagName;
element.tagName = value;
```

## <span>Examples</span>

This example retrieves the tag name of an object that has the identifier specified in the prompt window.

``` html
<SCRIPT>
var idValue = window.prompt("Get the tag with this ID:");
if (idValue != null) {
    alert(document.all[idValue].tagName)
}
</SCRIPT>
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
