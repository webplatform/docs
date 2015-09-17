---
title: 'window.location.href'
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
summary: 'The full url for this resource. Synonymous with String(window.location).'
tags:
  - API_Object_Properties
  - JavaScript
uri: apis/location/href

---
## Summary

The full url for this resource. Synonymous with String(window.location).

Property of [apis/location](/apis/location)[apis/location](/apis/location)

## Syntax

**Note**: This property is read-only.

``` js
var result = window.location.href;
```

## Return Value

Returns an object of type StringString

The full url for this resource.

For example, `http://example.org/index.html?page=1#foo` would return the full href of `http://example.org/index.html?page=1#foo`.

## Examples

`window.location.href` is the same as the `toString` method of `window.location`, so you can choose to use either variable when using comparing as a string.

``` js
if(window.location == window.location.href){
    // This equates to true
    alert("These values are the same.")/
}
```

## Related specifications

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
