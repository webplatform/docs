---
title: URL
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'should be document.URL not window>URL'
summary: 'Sets or gets the URL for the current document.'
uri: dom/Window/URL

---
# URL

## Summary

Sets or gets the URL for the current document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Window](/dom/Window)</span></span>

## Syntax

``` {.js}
var string = document.URL;
document.URL = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

the URL of the current web document.

## Examples

This example function returns the **URL** property of the current document.

``` {.js}
function getURL()
{
    return document.URL;
}
```

## Notes

### Remarks

The **URL** property is case-sensitive. This property is an alias for the [**location**](/dom/Location).[**href**](/dom/Location/href) property on the window.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.4

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[document.URL](https://developer.mozilla.org/en-US/docs/Web/API/document.URL) Article]

Portions of this content come from the Microsoft Developer Network: [[URL Property](http://msdn.microsoft.com/en-us/library/ie/ms534708(v=vs.85).aspx) Article]

