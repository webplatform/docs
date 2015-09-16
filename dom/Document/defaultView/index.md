---
title: defaultView
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'needs a better example and compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /dom/Document
standardization_status: 'W3C Working Draft'
summary: 'Returns the Document''s browsing context''s Window object (essentially the environment in which objects are presented to the user) if there is one, or null otherwise.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/defaultView

---
## Summary

Returns the Document's browsing context's Window object (essentially the environment in which objects are presented to the user) if there is one, or null otherwise.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var Window = document.defaultView;
document.defaultView = value;
```

## Return Value

Returns an object of type ObjectObject

Returns the Window object of the active document

## Examples

``` js
//displays the document's browsing context
function showDefView() {
    alert(document.defaultView);
}
```

## Related specifications

[HTML5 Specification](http://www.w3.org/TR/html5/browsers.html#window)
:   Working Draft

## See also

### Related pages (MSDN)

-   `Document`
