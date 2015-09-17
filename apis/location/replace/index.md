---
title: 'window.location.replace'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/location
    href: /apis/location
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/location
standardization_status: 'W3C Working Draft'
summary: 'Similar to window.location.assign, except that it &quot;replaces&quot; the current document, removing the previous one from the back button history.'
tags:
  - API_Object_Methods
  - JavaScript
uri: apis/location/replace

---
## Summary

Similar to window.location.assign, except that it &quot;replaces&quot; the current document, removing the previous one from the back button history.

Method of [apis/location](/apis/location)[apis/location](/apis/location)

## Syntax

``` js
var  = window.location.replace(url);
```

## Parameters

### url

 Data-type
:   String

 The new URL to navigate to.

## Return Value

Returns an object of type

## Examples

``` js
//force a new page to load and replace the current one
window.location.replace("http://www.example.com");
```

## Notes

It is generally advisable to use `window.location.assign` becuse it retains the back button history. The `replace` method removes the current page from the back history, and therefore may confuse the user.

## Related specifications

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
