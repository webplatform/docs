---
title: host
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'standards, compatibility, move MSDN content into WPD sections'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Location
    href: /dom/Location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Location
summary: 'Sets or retrieves the hostname and port number of the location or URL.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Location/host

---
## <span>Summary</span>

Sets or retrieves the hostname and port number of the location or URL.

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## <span>Syntax</span>

``` js
var host = location.host;
location.host = value;
```

## <span>Return Value</span>

Returns an object of type StringString

The host component of the URL.

## <span>Examples</span>

This example function returns the **host** property of the current page location.

``` js
function getHost() {
    return document.location.host;
}
```

## <span>Notes</span>

### <span>Remarks</span>

The **host** property is the concatenation of the [**hostname**](/dom/Location/hostname) and [**port**](/dom/Location/port) properties, separated by a colon (hostname:port). When the **port** property is **null**, the **host** property is the same as the **hostname** property. The **host** property may be set at any time, although it is safer to set the [**href**](/dom/Location/href) property to change a location. If the specified host cannot be found, an error is returned.