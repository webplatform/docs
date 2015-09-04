---
title: hostname
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The hostname property contains the hostname the current document was served from, excluding protocol, port, and other information.'
uri: apis/location/hostname

---
# window.location.hostname

## Summary

The hostname property contains the hostname the current document was served from, excluding protocol, port, and other information.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.location.hostname;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The hostname the current document was served from.

For example, `http://example.org/` would return the hostname `example.org`.

## Examples

The following example assumes your document has a div element with id 'hostDiv', like this.

``` {.js}
// Get the hostname from window.location
var hostnm = window.location.hostname;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the hostname
container.innerHTML = hostnm;
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

