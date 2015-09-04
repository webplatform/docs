---
title: defaultCharset
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: Non-Standard
notes:
  - 'Needs a note that this is not a W3C standard and does not work in most browsers, also needs compat table'
summary: 'Gets the default character set from the current regional language settings.'
uri: dom/Document/defaultCharset

---
# defaultCharset

## Summary

Gets the default character set from the current regional language settings.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var defaultCharacterSet = document.defaultCharset;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The name of the default character set of the user.

## Examples

``` {.js}
//displays the document's default character encoding string
function showDefCharSet() {
    alert(document.defaultCharset);
}
```

## Notes

The value depends on the current regional language settings. For typical settings in North America, the value is `windows-1252`.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

