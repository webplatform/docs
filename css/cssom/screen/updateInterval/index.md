---
title: updateInterval
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: css/cssom/screen/updateInterval

---
# updateInterval

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/screen](/css/cssom/screen)</span></span>

## Syntax

``` {.js}
var result = element.updateInterval;
element.updateInterval = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The **updateInterval** property can be set to an integer value specifying the number of milliseconds between updates to the screen. A value of `0` (the default) disables the update interval. The interval causes screen updates to be buffered and then drawn in the specified millisecond intervals. This limits excessive invalidations that reduce the overall painting performance, which can happen when too many flipbook-style animations occur at once. Use this property judiciously; a value too small or too large adversely affects the page rendering response.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `screen`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

