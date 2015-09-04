---
title: protocol
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "Sets or retrieves the protocol portion of a URL.\nThe protocol the current document was accessed via (everything preceding the \"//\").\n"
uri: apis/location/protocol

---
# window.location.protocol

## Summary

Sets or retrieves the protocol portion of a URL. The protocol the current document was accessed via (everything preceding the "//").

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.location.protocol;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The protocol the current document was accessed via.

For example, `http://example.org/` would return the protocol `http:`.

## Examples

The following example assumes your document has a div element with id 'hostDiv', like this.

``` {.js}
// Get the protocol from window.location
var hostpr = window.location.protocol;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the host protocol
container.innerHTML = hostpr;
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
[URL](http://www.w3.org/TR/url/#concept-url)
:   W3C Working Draft

