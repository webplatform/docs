---
title: responseText
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns the text response entity body, a string representing the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).'
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
uri: apis/xhr/XMLHttpRequest/responseText

---
## <span>Summary</span>

Returns the text response entity body, a string representing the response entity body, which is the fragment of the entity body of the response received so far (if LOADING) or the complete entity body of the response (if DONE).

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.responseText;
```

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

``` js
// receive data sent from the server

xhr.onreadystatechange = function(){
    if(xhr.readyState == 4){
        var responseText = xhr.responseText;
    }
}
```

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
