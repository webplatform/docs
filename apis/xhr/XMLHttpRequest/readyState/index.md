---
title: readyState
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Returns the current state of the XMLHttpRequest.'
tags:
  0: API
  1: Object
  2: Properties
  4: XHR
uri: apis/xhr/XMLHttpRequest/readyState

---
## <span>Summary</span>

Returns the current state of the XMLHttpRequest.

Property of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var state = xhr.readyState;
```

## <span>Return Value</span>

Returns an object of type unsigned shortunsigned short

Returns one of the following values:

-   UNSENT (0): [**open()**](/apis/xhr/XMLHttpRequest/open) has not been called yet.
-   OPENED (1): [**send()**](/apis/xhr/XMLHttpRequest/send) has not been called yet.
-   HEADERS\_RECEIVED (2): [**send()**](/apis/xhr/XMLHttpRequest/send) has been called, and headers and status are available.
-   LOADING (3): Downloading; [**responseText**](/apis/xhr/XMLHttpRequest/responseText) holds partial data.
-   DONE (4): The operation is complete.

## <span>Examples</span>

Prints a message to the console log during each state of the request.

``` js
function handler() {
  if (xhr.readyState === xhr.UNSENT) {
    console.log('XHR Unsent');
  } else if (xhr.readyState === xhr.OPENED) {
    console.log('XHR Opened');
  } else if (xhr.readyState === xhr.HEADERS_RECEIVED) {
    console.log('XHR Headers received');
  } else if (xhr.readyState === xhr.LOADING) {
    console.log('XHR Loading');
  } else if (xhr.readyState === xhr.DONE) {
    console.log('XHR Done');
  }
}

var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange = handler;
xhr.send();
```

## <span>Notes</span>

You cannot call the **responseText** property to obtain partial results (**readyState** = 3). Doing so will return an error, because the response is not fully received. You must wait until all data has been received. See [**onreadystatechange**](/apis/xhr/XMLHttpRequest/readystatechange).

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
