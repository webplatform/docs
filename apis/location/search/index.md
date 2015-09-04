---
title: search
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The search property contains the query string portion of the current url.'
uri: apis/location/search

---
# window.location.search

## Summary

The search property contains the query string portion of the current url.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.location.search;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The query string portion of the URL. This includes the question mark, and everything following, excluding the [hash](/apis/location/hash).

For example, `http://example.org/?page=1&mode=b#foo` would return the query string `?page=1&mode=b`.

## Examples

The following example assumes your document has a div element with id 'hostDiv', like this.

``` {.js}
// Get the query string from window.location
var hostqs = window.location.search;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the query string
container.innerHTML = hostqs;
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

