---
title: 'overrideMimeType'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Overrides the MIME type returned by the server.'
tags:
  - API_Object_Methods
  - API
  - XHR
uri: apis/xhr/XMLHttpRequest/overrideMimeType

---
## Summary

Overrides the MIME type returned by the server.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

``` js
 .overrideMimeType();
```

## Return Value

No return value

## Examples

``` js
function handler() {
  if (xhr.readyState === 4 /* complete */) {
    if (xhr.status === 200) {
            console.log(xhr.responseText);
        }
    }
}

var xhr = new XMLHttpRequest();
xhr.overrideMimeType("text/xml");
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange = handler;
xhr.send();
```

## Notes

This method may be used (for example) to force a returned stream to be treated and parsed as text/xml, even if the server does not report it as such. If used, this method must be called before send().

## Related specifications

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
