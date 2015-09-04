---
title: pixelDepth
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, example, spec reference, standardization status'
uri: css/cssom/screen/pixelDepth

---
# pixelDepth

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/screen](/css/cssom/screen)</span></span>

## Syntax

``` {.js}
var result = element.pixelDepth;
element.pixelDepth = value;
```

**Needs Examples**: This section should include examples.

## Notes

### Remarks

If you retrieve the value of the **pixelDepth** property through a script, you can select an appropriate color to return to the browser. If [**bufferDepth**](/css/cssom/screen/bufferDepth) is 0 or -1, **pixelDepth** is equal to the bits-per-pixel value for the screen or printer. If **pixelDepth** does not equal zero, **pixelDepth** is equal to [**colorDepth**](/css/cssom/screen/colorDepth).

### Syntax

### Standards information

-   [CSSOM View Module](http://go.microsoft.com/fwlink/p/?linkid=199793), 4.2

## See also

### Related pages (MSDN)

-   `screen`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

