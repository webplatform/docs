---
title: response status codes
uri: 'http/response status codes'

---
The IANA maintains the [Hypertext Transfer Protocol (HTTP) Status Code Registry](http://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)

## 1xx: Informational

Request received, continuing process

|Code|Status|Description|Defining Reference|
|:---|:-----|:----------|:-----------------|
|100|Continue||[RFC7231](http://www.iana.org/go/rfc7231)|
|101|Switching Protocols||[RFC7231](http://www.iana.org/go/rfc2616)|
|102|Processing||[RFC2518](http://www.iana.org/go/rfc2518)|

## 2xx: Success

The action was successfully received, understood, and accepted

|Code|Status|Description|Defining Reference|
|:---|:-----|:----------|:-----------------|
|200|OK||[RFC7231, Section 6.3.1](http://www.iana.org/go/rfc7231)|
|201|Created|The request succeeded and resulted in a new resource being created|[RFC7231, Section 6.3.2](http://www.iana.org/go/rfc7231)|
|202|Accepted|The request has been accepted, but will be processed at a later time|[RFC7231, Section 6.3.3](http://www.iana.org/go/rfc7231)|
|203|Non-Authoritative Information|A response is made using information for which another server is the authoritative source|[RFC7231, Section 6.3.4](http://www.iana.org/go/rfc7231)|
|204|No Content|The request succeeded and no entity-body needs to be returned, though information might be sent in headers|[RFC7231, Section 6.3.5](http://www.iana.org/go/rfc7231)|
|205|Reset Content|The request succeeded and the user-agent should take the user back to the start to enter another request|[RFC7231, Section 6.3.6](http://www.iana.org/go/rfc7231)|
|206|Partial Content|The response contains only a subset of the entire resource|[RFC7233, Section 4.1](http://www.iana.org/go/rfc7233)|
|207|Multi-Status||[RFC4918](http://www.iana.org/go/rfc4918)|
|208|Already Reported||[RFC5842](http://www.iana.org/go/rfc5842)|
|226|IM Used||[RFC3229](http://www.iana.org/go/rfc3229)|

## 3xx: Redirection

Further action must be taken in order to complete the request

|Code|Status|Description|Defining Reference|
|:---|:-----|:----------|:-----------------|
|300|Multiple Choices|The requested resource corresponds to any one of a set of representations|[RFC7231, Section 6.4.1](http://www.iana.org/go/rfc7231)|
|301|Moved Permanently|The requested resource has been assigned a new permanent URI|[RFC7231, Section 6.4.2](http://www.iana.org/go/rfc7231)|
|302|Found|The requested resource resides temporarily under a different URI (with ambiguous behavior, 307 is suggested instead)|[RFC7231, Section 6.4.3](http://www.iana.org/go/rfc7231)|
|303|See Other|The response to the request can be found under a different URI and SHOULD be retrieved using a GET method on that resource|[RFC7231, Section 6.4.4](http://www.iana.org/go/rfc7231)|
|304|Not Modified|The request is successful, and no entity-body is sent because the user-agent's cached version is up to date|[RFC7232, Section 4.1](http://www.iana.org/go/rfc7232)|
|305|Use Proxy|The requested resource MUST be accessed through the proxy given by the Location field (deprecated)|[RFC7231, Section 6.4.5](http://www.iana.org/go/rfc7231)|
|306|Reserved|(Unused)|[RFC7231, Section 6.4.6](http://www.iana.org/go/rfc7231)|
|307|Temporary Redirect|The request should be re-made to a different URI|[RFC7231, Section 6.4.7](http://www.iana.org/go/rfc7231)|
|308|Permanent Redirect|The request should be re-made to the resource's new URI|[RFC7238](http://www.iana.org/go/rfc7238)|

## 4xx: Client Error

The request contains bad syntax or cannot be fulfilled

|Code|Status|Description|Defining Reference|
|:---|:-----|:----------|:-----------------|
|400|Bad Request|The server cannot process the request due to a client error|[RFC7231, Section 6.5.1](http://www.iana.org/go/rfc7231)|
|401|Unauthorized|The request lacks valid authentication credentials|[RFC7235, Section 3.1](http://www.iana.org/go/rfc7235)|
|402|Payment Required|(Unused)|[RFC7231, Section 6.5.2](http://www.iana.org/go/rfc7231)|
|403|Forbidden|The server understood the request but refuses to authorize it|[RFC7231, Section 6.5.3](http://www.iana.org/go/rfc7231)|
|404|Not Found|The server does not know about such a resource|[RFC7231, Section 6.5.4](http://www.iana.org/go/rfc7231)|
|405|Method Not Allowed|The request method can't be applied to the resource|[RFC7231, Section 6.5.5](http://www.iana.org/go/rfc7231)|
|406|Not Acceptable||[RFC7231, Section 6.5.6](http://www.iana.org/go/rfc7231)|
|407|Proxy Authentication Required|The client must authenticate itself to the proxy|[RFC7235, Section 3.2](http://www.iana.org/go/rfc7235)|
|408|Request Timeout|The server didn't receive a complete request in a timely manner|[RFC7231, Section 6.5.7](http://www.iana.org/go/rfc7231)|
|409|Conflict|The request could not be completed due to a conflict with the current state of the target resource|[RFC7231, Section 6.5.8](http://www.iana.org/go/rfc7231)|
|410|Gone|The requested resource no longer exists|[RFC7231, Section 6.5.9](http://www.iana.org/go/rfc7231)|
|411|Length Required|The server refuses to accept an upload without being told its Content-Length|[RFC7231, Section 6.5.10](http://www.iana.org/go/rfc7231)|
|412|Precondition Failed|The request was not processed because conditions requested by the client were evaluated false by the server|[RFC7232, Section 4.2](http://www.iana.org/go/rfc7232)|
|413|Request Entity Too Large|the request payload is larger than the server is willing or able to process|[RFC7231, Section 6.5.11](http://www.iana.org/go/rfc7231)|
|414|Request-URI Too Long|The request-target is longer than the server is willing to interpret|[RFC7231, Section 6.5.12](http://www.iana.org/go/rfc7231)|
|415|Unsupported Media Type|The payload is in a format not supported by this method on the target resource|[RFC7231, Section 6.5.13](http://www.iana.org/go/rfc7231)|
|416|Requested Range Not Satisfiable|A problem with the request's Range header|[RFC7233, Section 4.4](http://www.iana.org/go/rfc7233)|
|417|Expectation Failed|An expectation in the request Expect could not be filled by a server.|[RFC7231, Section 6.5.14](http://www.iana.org/go/rfc7231)|
|422|Unprocessable Entity||[RFC4918](http://www.iana.org/go/rfc4918)|
|423|Locked||[RFC4918](http://www.iana.org/go/rfc4918)|
|424|Failed Dependency||[RFC4918](http://www.iana.org/go/rfc4918)|
|426|Upgrade Required|The server might be able to fill the request after changing protocols|[RFC7231, Section 6.5.15](http://www.iana.org/go/rfc7231)|
|428|Precondition Required|The server requests a conditional request header such as If-Match to prevent "lost updates"|[RFC6585](http://www.iana.org/go/rfc6585)|
|429|Too Many Requests|The client has exceeded a request rate limit imposed by the server. Enhance your calm!|[RFC6585](http://www.iana.org/go/rfc6585)|
|431|Request Header Fields Too Large||[RFC6585](http://www.iana.org/go/rfc6585)|

## 5xx: Server Error

The server failed to fulfill an apparently valid request

|Code|Status|Description|Defining Reference|
|:---|:-----|:----------|:-----------------|
|500|Internal Server Error|The server encountered an unexpected condition that prevented it from fulfilling the request|[RFC7231, Section 6.6.1](http://www.iana.org/go/rfc7231)|
|501|Not Implemented|The server does not support the functionality required to fulfill the request|[RFC7231, Section 6.6.2](http://www.iana.org/go/rfc7231)|
|502|Bad Gateway|A server encountered a problem forwarding the request|[RFC7231, Section 6.6.3](http://www.iana.org/go/rfc7231)|
|503|Service Unavailable|The server is currently unable to handle the request due to a temporary overload or scheduled maintenance|[RFC7231, Section 6.6.4](http://www.iana.org/go/rfc7231)|
|504|Gateway Timeout|The server, while acting as a gateway or proxy, did not receive a timely response from an upstream server|[RFC7231, Section 6.6.5](http://www.iana.org/go/rfc7231)|
|505|HTTP Version Not Supported|The server does not support, or refuses to support, the major version of HTTP that was used in the request message|[RFC7231, Section 6.6.6](http://www.iana.org/go/rfc7231)|
|506|Variant Also Negotiates (Experimental)|Indicates an error in the server's configuration of Content-Type negotiation|[RFC2295](http://www.iana.org/go/rfc2295)|
|507|Insufficient Storage|The server encountered an internal error while storing data|[RFC4918](http://www.iana.org/go/rfc4918)|
|508|Loop Detected||[RFC5842](http://www.iana.org/go/rfc5842)|
|510|Not Extended|(Experimental)|[RFC2774](http://www.iana.org/go/rfc2774)|
|511|Network Authentication Required|For use by "captive portals"|[RFC6585](http://www.iana.org/go/rfc6585)|

