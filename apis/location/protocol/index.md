---
title: window.location.protocol
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
summary: "Sets or retrieves the protocol portion of a URL.\nThe protocol the current document was accessed via (everything preceding the &quot;//&quot;).\n"
tags:
  - API
  - Object
  - Properties
  - JavaScript
uri: apis/location/protocol

---
## <span>Summary</span>

Sets or retrieves the protocol portion of a URL. The protocol the current document was accessed via (everything preceding the &quot;//&quot;).

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = window.location.protocol;
```

## <span>Return Value</span>

Returns an object of type StringString

The protocol the current document was accessed via.

For example, `http://example.org/` would return the protocol `http:`.

## <span>Examples</span>

The following example assumes your document has a div element with id 'hostDiv', like this.

``` js
// Get the protocol from window.location
var hostpr = window.location.protocol;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the host protocol
container.innerHTML = hostpr;
```

## <span>Related specifications</span>

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

[URL](http://www.w3.org/TR/url/#concept-url)
:   W3C Working Draft
