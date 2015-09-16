---
title: URL
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[document.URL](https://developer.mozilla.org/en-US/docs/Web/API/document.URL) Article]'
  - 'Microsoft Developer Network: [[URL Property](http://msdn.microsoft.com/en-us/library/ie/ms534708(v=vs.85).aspx) Article]'
notes:
  - 'should be document.URL not window>URL'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Window
standardization_status: 'W3C Recommendation'
summary: 'Sets or gets the URL for the current document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/URL

---
## Summary

Sets or gets the URL for the current document.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var string = document.URL;
document.URL = value;
```

## Return Value

Returns an object of type StringString

the URL of the current web document.

## Examples

This example function returns the **URL** property of the current document.

``` js
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
