---
title: window.location.host
code_samples:
  - 'http://fiddle.jshell.net/YJEhh/4/'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/location
    href: /apis/location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/location
standardization_status: 'W3C Working Draft'
summary: 'The host property contains the host part of the the current document URL, (hostname:port).'
tags:
  - API
  - Object
  - Properties
  - JavaScript
uri: apis/location/host

---
## Summary

The host property contains the host part of the the current document URL, (hostname:port).

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## Syntax

**Note**: This property is read-only.

``` js
var result = window.location.host;
```

## Return Value

Returns an object of type StringString

The hostname and port number.

For example, `http://example.org:8080/` would return the host string of `example.org:8080`.

## Examples

The following example assumes your document has a div element with id 'hostDiv', like this.

``` js
// Get the host from window.location
var host = window.location.host;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the host
container.innerHTML = host;
```

[View live example](http://fiddle.jshell.net/YJEhh/4/)

## Related specifications

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
