---
title: elementFromPoint
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs mobile compat'
summary: 'Returns the element at the specified x and y coordinates.'
uri: dom/Document/elementFromPoint

---
# elementFromPoint

## Summary

Returns the element at the specified x and y coordinates.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var element = document.elementFromPoint(x, y);
```

## Parameters

### x

 Data-typeÂ
:   double

 A numberÂ that specifies the X-offset, in pixels. Zero-based.

### y

 Data-typeÂ
:   double

 A number that specifies the Y-offset, in pixels. Zero-based.

## Return Value

Returns an object of type DOM Node.

The element at the given point.

## Examples

Listen for click event on entire document, log nodeName of element found with elementFromPoint()

``` {.js}
document.addEventListener("click", function(event){
  var el = document.elementFromPoint(event.clientX, event.clientY);
  console.log(el.nodeName);
});
```

## Usage

     This methods is used to get the element from the document whose elementFromPoint method is being called which is the topmost element which lies under the given point.  To get an element, specify the point via coordinates, in CSS pixels, relative to the upper-left-most point in the window or frame containing the document.

## Notes

Coordinates are supplied in client coordinates. The upper-left corner of the client area is (0,0). For **elementFromPoint** to exhibit expected behavior, the object or element located at position (x, y) must support and respond to mouse events.

## Related specifications

Specification
:   Status
[CSSOM View Module](http://dev.w3.org/csswg/cssom-view/#widl-Document-elementFromPoint-Element-float-x-float-y)
:   Editor's Draft 3

## See also

### Related pages (MSDN)

-   `clientX`
-   `clientY`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/DOM/document.elementFromPoint)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

