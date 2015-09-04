---
title: port
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The port number the document was accessed via.'
uri: apis/location/port

---
# window.location.port

## Summary

The port number the document was accessed via.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.location.port;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

The port number the document was accessed via.

For example, `http://example.org/` would return the default HTTP port number of `80`.

## Examples

The following example assumes your document has a div element with id 'hostDiv', like this.

``` {.js}
// Get the port from window.location
var host = window.location.port;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the port
container.innerHTML = port;
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

