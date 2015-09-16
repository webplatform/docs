---
title: updateInterval
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/screen
    href: /css/cssom/screen
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/screen/updateInterval

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/cssom/screen](/css/cssom/screen)[css/cssom/screen](/css/cssom/screen)

## Syntax

``` js
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
