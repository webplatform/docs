---
title: host
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'standards, compatibility, move MSDN content into WPD sections'
summary: 'Sets or retrieves the hostname and port number of the location or URL.'
uri: dom/Location/host

---
# host

## Summary

Sets or retrieves the hostname and port number of the location or URL.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Location](/dom/Location)</span></span>

## Syntax

``` {.js}
var host = location.host;
location.host = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The host component of the URL.

## Examples

This example function returns the **host** property of the current page location.

``` {.js}
function getHost() {
    return document.location.host;
}
```

## Notes

### Remarks

The **host** property is the concatenation of the [**hostname**](/dom/Location/hostname) and [**port**](/dom/Location/port) properties, separated by a colon (hostname:port). When the **port** property is **null**, the **host** property is the same as the **hostname** property. The **host** property may be set at any time, although it is safer to set the [**href**](/dom/Location/href) property to change a location. If the specified host cannot be found, an error is returned.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

