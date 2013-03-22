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
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 101
| Switching Protocols
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 102
| Processing
| 
| [http://www.iana.org/go/rfc2518 rfc2518]
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
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 201
| Created
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 202
| Accepted
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 203
| Non-Authoritative Information
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 204
| No Content
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 205
| Reset Content
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 206
| Partial Content
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 207
| Multi-Status
| 
| [http://www.iana.org/go/rfc4918 rfc4918]
|-
| 208
| Already Reported
| 
| [http://www.iana.org/go/rfc5842 rfc5842]
|-
| 226
| IM Used
| 
| [http://www.iana.org/go/rfc3229 rfc3229]
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
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 301
| Moved Permanently
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 302
| Found
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 303
| See Other
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 304
| Not Modified
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 305
| Use Proxy
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 306
| Reserved
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 307
| Temporary Redirect
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 308
| Permanent Redirect
| 
| [http://www.iana.org/go/RFC-reschke-http-status-308-07 RFC-reschke-http-status-308-07]
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
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 401
| Unauthorized
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 402
| Payment Required
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 403
| Forbidden
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 404
| Not Found
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 405
| Method Not Allowed
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 406
| Not Acceptable
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 407
| Proxy Authentication Required
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 408
| Request Timeout
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 409
| Conflict
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 410
| Gone
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 411
| Length Required
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 412
| Precondition Failed
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 413
| Request Entity Too Large
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 414
| Request-URI Too Long
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 415
| Unsupported Media Type
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 416
| Requested Range Not Satisfiable
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 417
| Expectation Failed
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 422
| Unprocessable Entity
| 
| [http://www.iana.org/go/rfc4918 rfc4918]
|-
| 423
| Locked
| 
| [http://www.iana.org/go/rfc4918 rfc4918]
|-
| 424
| Failed Dependency
| 
| [http://www.iana.org/go/rfc4918 rfc4918]
|-
| 426
| Upgrade Required
| 
| [http://www.iana.org/go/rfc2817 rfc2817]
|-
| 428
| Precondition Required
| 
| [http://www.iana.org/go/rfc6585 rfc6585]
|-
| 429
| Too Many Requests
| 
| [http://www.iana.org/go/rfc6585 rfc6585]
|-
| 431
| Request Header Fields Too Large
| 
| [http://www.iana.org/go/rfc6585 rfc6585]
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
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 501
| Not Implemented
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 502
| Bad Gateway
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 503
| Service Unavailable
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 504
| Gateway Timeout
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 505
| HTTP Version Not Supported
| 
| [http://www.iana.org/go/rfc2616 rfc2616]
|-
| 506
| Variant Also Negotiates (Experimental)
| 
| [http://www.iana.org/go/rfc2295 rfc2295]
|-
| 507
| Insufficient Storage
| 
| [http://www.iana.org/go/rfc4918 rfc4918]
|-
| 508
| Loop Detected
| 
| [http://www.iana.org/go/rfc5842 rfc5842]
|-
| 510
| Not Extended
| 
| [http://www.iana.org/go/rfc2774 rfc2774]
|-
| 511
| Network Authentication Required
| 
| [http://www.iana.org/go/rfc6585 rfc6585]
|}