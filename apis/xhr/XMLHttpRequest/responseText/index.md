---
title: responseText
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Returns the text response entity body, a string representing the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).'
uri: apis/xhr/XMLHttpRequest/responseText

---
# responseText

## Summary

Returns the text response entity body, a string representing the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.responseText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

``` {.js}
// receive data sent from the server

xhr.onreadystatechange = function(){
    if(xhr.readyState == 4){
        var responseText = xhr.responseText;
    }
}
```

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

