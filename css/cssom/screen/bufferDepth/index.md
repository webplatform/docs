---
title: bufferDepth
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: css/cssom/screen/bufferDepth

---
# bufferDepth

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/screen](/css/cssom/screen)</span></span>

## Syntax

``` {.js}
var result = element.bufferDepth;
element.bufferDepth = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Nonsupported values cause **bufferDepth** to be set to **-1**. When **bufferDepth** is **-1** and the user changes system settings that affect the screen depth, the buffer depth is automatically updated to the new depth. This is not the case if **bufferDepth** is set to a specific value.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `screen`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

