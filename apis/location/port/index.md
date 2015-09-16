---
title: 'window.location.port'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/location
    href: /apis/location
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/location
standardization_status: 'W3C Working Draft'
summary: 'The port number the document was accessed via.'
tags:
  - API
  - Object
  - Properties
  - JavaScript
uri: apis/location/port

---
## Summary

The port number the document was accessed via.

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## Syntax

**Note**: This property is read-only.

``` js
var result = window.location.port;
```

## Return Value

Returns an object of type

The port number the document was accessed via.

For example, `http://example.org/` would return the default HTTP port number of `80`.

## Examples

The following example assumes your document has a div element with id 'hostDiv', like this.

``` js
// Get the port from window.location
var host = window.location.port;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the port
container.innerHTML = port;
```

## Related specifications

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
