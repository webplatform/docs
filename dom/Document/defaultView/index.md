---
title: defaultView
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'needs a better example and compat table'
summary: 'Returns the Document''s browsing context''s Window object (essentially the environment in which objects are presented to the user) if there is one, or null otherwise.'
uri: dom/Document/defaultView

---
# defaultView

## Summary

Returns the Document's browsing context's Window object (essentially the environment in which objects are presented to the user) if there is one, or null otherwise.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var Window = document.defaultView;
document.defaultView = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

Returns the Window object of the active document

## Examples

``` {.js}
//displays the document's browsing context
function showDefView() {
    alert(document.defaultView);
}
```

## Related specifications

Specification
:   Status
[HTML5 Specification](http://www.w3.org/TR/html5/browsers.html#window)
:   Working Draft

## See also

### Related pages (MSDN)

-   `Document`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

