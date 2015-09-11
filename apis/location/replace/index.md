---
title: window.location.replace
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
  - API
  - Object
  - Methods
  - JavaScript
uri: apis/location/replace

---
## <span>Summary</span>

Similar to window.location.assign, except that it &quot;replaces&quot; the current document, removing the previous one from the back button history.

Method of [apis/location](/apis/location)[apis/location](/apis/location)

## <span>Syntax</span>

``` js
var  = window.location.replace(url);
```

## <span>Parameters</span>

### <span>url</span>

 Data-type
:   String

 The new URL to navigate to.

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
//force a new page to load and replace the current one
window.location.replace("http://www.example.com");
```

## <span>Notes</span>

It is generally advisable to use `window.location.assign` becuse it retains the back button history. The `replace` method removes the current page from the back history, and therefore may confuse the user.

## <span>Related specifications</span>

[Window Object 1.0](http://www.w3.org/TR/Window/)
:   W3C Working Draft
