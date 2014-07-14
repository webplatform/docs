
The IANA maintains the [http://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml Hypertext Transfer Protocol (HTTP) Status Code Registry]



==1xx: Informational==
Request received, continuing process

{|
! Code
! Status
! Description
! Defining Reference
|-
| 100
| Continue
| 
| [http://www.iana.org/go/rfc7231 RFC7231]
|-
| 101
| Switching Protocols
| 
| [http://www.iana.org/go/rfc2616 RFC7231]
|-
| 102
| Processing
| 
| [http://www.iana.org/go/rfc2518 RFC2518]
|}

==2xx: Success==
The action was successfully received, understood, and accepted

{|
! Code
! Status
! Description
! Defining Reference
|-
| 200
| OK
| 
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.3.1]
|-
| 201
| Created
| The request succeeded and resulted in a new resource being created
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.3.2]
|-
| 202
| Accepted
| The request has been accepted, but will be processed at a later time
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.3.3]
|-
| 203
| Non-Authoritative Information
| A response is made using information for which another server is the authoritative source
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.3.4]
|-
| 204
| No Content
| The request succeeded and no entity-body needs to be returned, though information might be sent in headers
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.3.5]
|-
| 205
| Reset Content
| The request succeeded and the user-agent should take the user back to the start to enter another request
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.3.6]
|-
| 206
| Partial Content
| The response contains only a subset of the entire resource
| [http://www.iana.org/go/rfc7233 RFC7233, Section 4.1]
|-
| 207
| Multi-Status
| 
| [http://www.iana.org/go/rfc4918 RFC4918]
|-
| 208
| Already Reported
| 
| [http://www.iana.org/go/rfc5842 RFC5842]
|-
| 226
| IM Used
| 
| [http://www.iana.org/go/rfc3229 RFC3229]
|}

==3xx: Redirection==
Further action must be taken in order to complete the request

{|
! Code
! Status
! Description
! Defining Reference
|-
| 300
| Multiple Choices
| The requested resource corresponds to any one of a set of representations
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.4.1]
|-
| 301
| Moved Permanently
| The requested resource has been assigned a new permanent URI
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.4.2]
|-
| 302
| Found
| The requested resource resides temporarily under a different URI (with ambiguous behavior, 307 is suggested instead)
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.4.3]
|-
| 303
| See Other
| The response to the request can be found under a different URI and SHOULD be retrieved using a GET method on that resource
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.4.4]
|-
| 304
| Not Modified
| The request is successful, and no entity-body is sent because the user-agent's cached version is up to date
| [http://www.iana.org/go/rfc7232 RFC7232, Section 4.1]
|-
| 305
| Use Proxy
| The requested resource MUST be accessed through the proxy given by the Location field (deprecated)
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.4.5]
|-
| 306
| Reserved
| (Unused)
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.4.6]
|-
| 307
| Temporary Redirect
| The request should be re-made to a different URI
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.4.7]
|-
| 308
| Permanent Redirect
| The request should be re-made to the resource's new URI
| [http://www.iana.org/go/rfc7238 RFC7238]
|}

==4xx: Client Error==
The request contains bad syntax or cannot be fulfilled

{|
! Code
! Status
! Description
! Defining Reference
|-
| 400
| Bad Request
| The server cannot process the request due to a client error
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.1]
|-
| 401
| Unauthorized
| The request lacks valid authentication credentials
| [http://www.iana.org/go/rfc7235 RFC7235, Section 3.1]
|-
| 402
| Payment Required
| (Unused)
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.2]
|-
| 403
| Forbidden
| The server understood the request but refuses to authorize it
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.3]
|-
| 404
| Not Found
| The server does not know about such a resource
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.4]
|-
| 405
| Method Not Allowed
| The request method can't be applied to the resource
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.5]
|-
| 406
| Not Acceptable
| 
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.6]
|-
| 407
| Proxy Authentication Required
| The client must authenticate itself to the proxy
| [http://www.iana.org/go/rfc7235 RFC7235, Section 3.2]
|-
| 408
| Request Timeout
| The server didn't receive a complete request in a timely manner
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.7]
|-
| 409
| Conflict
| The request could not be completed due to a conflict with the current state of the target resource
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.8]
|-
| 410
| Gone
| The requested resource no longer exists
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.9]
|-
| 411
| Length Required
| The server refuses to accept an upload without being told its Content-Length
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.10]
|-
| 412
| Precondition Failed
| The request was not processed because conditions requested by the client were evaluated false by the server
| [http://www.iana.org/go/rfc7232 RFC7232, Section 4.2]
|-
| 413
| Request Entity Too Large
| the request payload is larger than the server is willing or able to process
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.11]
|-
| 414
| Request-URI Too Long
| The request-target is longer than the server is willing to interpret
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.12]
|-
| 415
| Unsupported Media Type
| The payload is in a format not supported by this method on the target resource
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.13]
|-
| 416
| Requested Range Not Satisfiable
| A problem with the request's Range header
| [http://www.iana.org/go/rfc7233 RFC7233, Section 4.4]
|-
| 417
| Expectation Failed
| An expectation in the request Expect could not be filled by a server.
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.14]
|-
| 422
| Unprocessable Entity
| 
| [http://www.iana.org/go/rfc4918 RFC4918]
|-
| 423
| Locked
| 
| [http://www.iana.org/go/rfc4918 RFC4918]
|-
| 424
| Failed Dependency
| 
| [http://www.iana.org/go/rfc4918 RFC4918]
|-
| 426
| Upgrade Required
| The server might be able to fill the request after changing protocols
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.5.15]
|-
| 428
| Precondition Required
| 
| [http://www.iana.org/go/rfc6585 RFC6585]
|-
| 429
| Too Many Requests
| 
| [http://www.iana.org/go/rfc6585 RFC6585]
|-
| 431
| Request Header Fields Too Large
| 
| [http://www.iana.org/go/rfc6585 RFC6585]
|}

==5xx: Server Error==
The server failed to fulfill an apparently valid request

{|
! Code
! Status
! Description
! Defining Reference
|-
| 500
| Internal Server Error
| The server encountered an unexpected condition that prevented it from fulfilling the request
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.6.1]
|-
| 501
| Not Implemented
| The server does not support the functionality required to fulfill the request
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.6.2]
|-
| 502
| Bad Gateway
| A server encountered a problem forwarding the request
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.6.3]
|-
| 503
| Service Unavailable
| The server is currently unable to handle the request due to a temporary overload or scheduled maintenance
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.6.4]
|-
| 504
| Gateway Timeout
| The server, while acting as a gateway or proxy, did not receive a timely response from an upstream server
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.6.5]
|-
| 505
| HTTP Version Not Supported
| The server does not support, or refuses to support, the major version of HTTP that was used in the request message
| [http://www.iana.org/go/rfc7231 RFC7231, Section 6.6.6]
|-
| 506
| Variant Also Negotiates (Experimental)
| Indicates an error in the server's configuration of Content-Type negotiation
| [http://www.iana.org/go/rfc2295 RFC2295]
|-
| 507
| Insufficient Storage
| The server encountered an internal error while storing data
| [http://www.iana.org/go/rfc4918 RFC4918]
|-
| 508
| Loop Detected
| 
| [http://www.iana.org/go/rfc5842 RFC5842]
|-
| 510
| Not Extended
| (Experimental)
| [http://www.iana.org/go/rfc2774 RFC2774]
|-
| 511
| Network Authentication Required
| For use by "captive portals"
| [http://www.iana.org/go/rfc6585 RFC6585]
|}