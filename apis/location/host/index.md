---
title: host
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The host property contains the host part of the the current document URL, (hostname:port).'
code_samples:
  - 'http://fiddle.jshell.net/YJEhh/4/'
uri: apis/location/host

---
# window.location.host

## Summary

The host property contains the host part of the the current document URL, (hostname:port).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.location.host;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The hostname and port number.

For example, `http://example.org:8080/` would return the host string of `example.org:8080`.

## Examples

The following example assumes your document has a div element with id 'hostDiv', like this.

``` {.js}
// Get the host from window.location
var host = window.location.host;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the host
container.innerHTML = host;
```

[View live example](http://fiddle.jshell.net/YJEhh/4/)

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

