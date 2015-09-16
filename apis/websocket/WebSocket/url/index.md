---
title: url
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/websocket/WebSocket
    href: /apis/websocket/WebSocket
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/websocket/WebSocket
standardization_status: 'W3C Candidate Recommendation'
summary: 'The absolute URL as resolved by the constructor.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebSocket
uri: apis/websocket/WebSocket/url

---
## Summary

The absolute URL as resolved by the constructor.

Property of [apis/websocket/WebSocket](/apis/websocket/WebSocket)[apis/websocket/WebSocket](/apis/websocket/WebSocket)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.url;
```

## Return Value

Returns an object of type StringString

The URL specifies the following details about the connection.

-   Scheme ― The scheme must be "ws" or "wss". The "ws" scheme is insecure, while "wss" indicates a secure connection. Pages that are served over HTTP should use "ws" WebSockets, while HTTPS pages should use "wss". Attempting to use a scheme other than "ws" or "wss" throws an error.
-   Host ― The host is the name or IP address of the server.
-   Port ― This specifies the remote port to connect to. If the port is not specified then a default is selected based on the scheme. "ws" connections default to port 80, while "wss" connections default to 443.
-   Resource Name ― The resource name is the path component of the URL which follows the host/port. This includes the URL query component (the part following a question mark), if one is present. The resource name can be omitted, in which case it defaults to a forward slash "/".

## Examples

Example URLs

``` js
scheme://host:port/resource
ws://localhost:8080/echo
wss://cjihrig.com
```

## Notes

You can use this property to make sure that the URL that is used for the connection is parsed the way the app expects.

## Related specifications

[W3C WebSocket Specification](http://www.w3.org/TR/websockets/)
:   W3C Candidate Recommendation
