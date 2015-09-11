---
title: window.location.search
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
summary: 'The search property contains the query string portion of the current url.'
tags:
  - API
  - Object
  - Properties
  - JavaScript
uri: apis/location/search

---
## <span>Summary</span>

The search property contains the query string portion of the current url.

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = window.location.search;
```

## <span>Return Value</span>

Returns an object of type StringString

The query string portion of the URL. This includes the question mark, and everything following, excluding the [hash](/apis/location/hash).

For example, `http://example.org/?page=1&mode=b#foo` would return the query string `?page=1&mode=b`.

## <span>Examples</span>

The following example assumes your document has a div element with id 'hostDiv', like this.

``` js
// Get the query string from window.location
var hostqs = window.location.search;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the query string
container.innerHTML = hostqs;
```

## <span>Related specifications</span>

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
