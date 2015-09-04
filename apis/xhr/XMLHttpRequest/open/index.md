---
title: open
tags:
  0: API
  1: Object
  2: Methods
  4: XHR
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Initializes an XMLHttpRequest.'
uri: apis/xhr/XMLHttpRequest/open

---
# open

## Summary

Initializes an XMLHttpRequest.

*Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)*

## Syntax

``` {.js}
 object.open(method, url, async, user, password);
```

## Parameters

### method

 Data-typeÂ
:   String

 Specifies the HTTP method used to open the connection, such as GET, POST, or HEAD. This parameter is not case-sensitive.

### url

 Data-typeÂ
:   String

 Specifies either an absolute or relative URL of the XML data or server-side Web services.

### async

 Data-typeÂ
:   Boolean

*(Optional)*

Specifies true for asynchronous operation (the call returns immediately), or false for synchronous operation. If true, assign a callback handler to the **onreadystatechange** property to determine when the call has completed. If not specified, the default is true.

### user

 Data-typeÂ
:   String

*(Optional)*

Specifies the name of the user for authentication. If this parameter is null or not specified and the site requires authentication, the browser displays a logon window.

### password

 Data-typeÂ
:   String

*(Optional)*

Specifies the password for authentication. This parameter is ignored if the user parameter is null or not specified.

## Return Value

No return value

## Examples

The following script demonstrates how to create and use the XMLHttpRequest object. For best client-side performance, the request is asynchronous and uses an onreadystatechange event handler to process the data returned by the call.

``` {.js}
function handler() {
  if (xhr.readyState === 4 /* complete */) {
    if (xhr.status === 200) {
            console.log(xhr.responseText);
        }
    }
}
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange = handler;
xhr.send();
```

## Notes

The following HTTP verbs and World Wide Web Distributed Authoring and Versioning (WebDAV) methods are supported:

Verb / Method
:   Defined In [HTTP (RFC-2616)](http://go.microsoft.com/fwlink/p/?linkid=84048)
GET
:   [HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)
POST
:   [HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)
HEAD
:   [HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)
PUT
:   [HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)
DELETE
:   [HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)
MOVE
:
PROPFIND
:
PROPPATCH
:
MKCOL
:
COPY
:
LOCK
:
UNLOCK
:
OPTIONS
:   [HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)

Internet Explorer caches the results of HTTP GET requests in the Temporary Internet Files (TIF) folder. In most cases, caching improves performance for data that will not change frequently. To guarantee that the results are not cached, use POST. **Security Warning:Â Â **Â Cross-domain, cross-port, and mixed protocol requests are not allowed. The *bstrUrl* parameter may only specify files in the same domain, using the same port and protocol method, as that from which the page is served. Although this method accepts credentials passed via parameter, those credentials are not automatically sent to the server on the first request. The *varUser* and *varPassword* parameters are not transmitted unless the server challenges the client for credentials with a 401 - Access Denied response. After calling this method, use **send** to send the request and data, if any, to the server.

## Related specifications

Specification
:   Status
[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

