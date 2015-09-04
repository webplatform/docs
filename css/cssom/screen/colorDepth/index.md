---
title: colorDepth
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: css/cssom/screen/colorDepth

---
# colorDepth

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/screen](/css/cssom/screen)</span></span>

## Syntax

``` {.js}
var result = element.colorDepth;
element.colorDepth = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Retrieving the value of the property through script enables you to select an appropriate color to return to the client. If [**bufferDepth**](/css/cssom/screen/bufferDepth) is 0 or -1, **colorDepth** is equal to the bits-per-pixel value for the screen or printer. If **bufferDepth** is nonzero, **colorDepth** is equal to **bufferDepth**.

### Syntax

### Standards information

-   [CSSOM View Module](http://go.microsoft.com/fwlink/p/?linkid=199793), 4.2

## See also

### Related pages (MSDN)

-   `screen`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

