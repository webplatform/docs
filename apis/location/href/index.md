---
title: href
tags:
  - API
  - Object
  - Properties
  - JavaScript
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The full url for this resource. Synonymous with String(window.location).'
uri: apis/location/href

---
# window.location.href

## Summary

The full url for this resource. Synonymous with String(window.location).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/location](/apis/location)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.location.href;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The full url for this resource.

For example, `http://example.org/index.html?page=1#foo` would return the full href of `http://example.org/index.html?page=1#foo`.

## Examples

`window.location.href` is the same as the `toString` method of `window.location`, so you can choose to use either variable when using comparing as a string.

``` {.js}
if(window.location == window.location.href){
    // This equates to true
    alert("These values are the same.")/
}
```

## Related specifications

Specification
:   Status
[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft

