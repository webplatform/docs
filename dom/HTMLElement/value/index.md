---
title: value
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'stub MSDN import'
uri: dom/HTMLElement/value

---
# value

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.value;
element.value = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Windows Internet Explorer 8 or later. In IE8 Standards mode, the **value** property is correctly reported as a canonical attribute name. For example, `<input type="text" readonly>` and `<input type="text" readonly="readonly">` would both set the input text field to read-only. In IE8 mode, the value is evaluated as a canonical value, `"readonly"`. In earlier document compatibility modes, it is evaluated as a Boolean value, true. For more information, see Attribute Differences in Internet Explorer 8. **value** was introduced in Microsoft Internet Explorer 6.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages (MSDN)

-   `attributes`
-   `nodeValue`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

