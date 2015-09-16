---
title: 'open'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Initializes an XMLHttpRequest.'
tags:
  0: API
  1: Object
  2: Methods
  4: XHR
uri: apis/xhr/XMLHttpRequest/open

---
## Summary

Initializes an XMLHttpRequest.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## Syntax

``` js
 object.open(method, url, async, user, password);
```

## Parameters

### method

 Data-type
:   String

 Specifies the HTTP method used to open the connection, such as GET, POST, or HEAD. This parameter is not case-sensitive.

### url

 Data-type
:   String

 Specifies either an absolute or relative URL of the XML data or server-side Web services.

### async

 Data-type
:   Boolean

(Optional)

Specifies true for asynchronous operation (the call returns immediately), or false for synchronous operation. If true, assign a callback handler to the **onreadystatechange** property to determine when the call has completed. If not specified, the default is true.

### user

 Data-type
:   String

(Optional)

Specifies the name of the user for authentication. If this parameter is null or not specified and the site requires authentication, the browser displays a logon window.

### password

 Data-type
:   String

(Optional)

Specifies the password for authentication. This parameter is ignored if the user parameter is null or not specified.

## Return Value

No return value

## Examples

The following script demonstrates how to create and use the XMLHttpRequest object. For best client-side performance, the request is asynchronous and uses an onreadystatechange event handler to process the data returned by the call.

``` js
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

|Verb / Method|Defined In [HTTP (RFC-2616)](http://go.microsoft.com/fwlink/p/?linkid=84048)|Defined In [WebDAV (RFC-2518)](http://go.microsoft.com/fwlink/p/?linkid=84046)|Function|
|:------------|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------|:-------|
|GET|[HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)|[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Request URI|
|POST|[HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)|[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Send data to server|
|HEAD|[HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)|[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Request URI without body|
|PUT|[HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)|[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Store data for URI|
|DELETE|[HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)|[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Delete data for URI|
|MOVE||[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Move URI to to new location|
|PROPFIND||[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Request URI Properties|
|PROPPATCH||[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Update or Delete URI Properties|
|MKCOL||[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Create collection at URI|
|COPY||[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Create copy of URI|
|LOCK||[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Create Lock|
|UNLOCK||[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Remove Lock|
|OPTIONS|[HTTP](http://go.microsoft.com/fwlink/p/?linkid=84048)|[WebDAV](http://go.microsoft.com/fwlink/p/?linkid=84046)|Request URI Options|

Internet Explorer caches the results of HTTP GET requests in the Temporary Internet Files (TIF) folder. In most cases, caching improves performance for data that will not change frequently. To guarantee that the results are not cached, use POST. **Security Warning:  ** Cross-domain, cross-port, and mixed protocol requests are not allowed. The *bstrUrl* parameter may only specify files in the same domain, using the same port and protocol method, as that from which the page is served. Although this method accepts credentials passed via parameter, those credentials are not automatically sent to the server on the first request. The *varUser* and *varPassword* parameters are not transmitted unless the server challenges the client for credentials with a 401 - Access Denied response. After calling this method, use **send** to send the request and data, if any, to the server.

## Related specifications

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
