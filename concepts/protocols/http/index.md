{{Page_Title|HTTP}}
{{Flags
|State=Not Ready
|Checked_Out=No
|High-level issues=Stub, Missing Relevant Sections
}}
{{Summary_Section|HTTP is an application-layer protocol used for storing, retrieving, and communicating about information resources on a remote server. It is the transfer protocol used by the Web, and defines many features to support caching, authentication, manipulation of resources, negotiation of functionality, and more.}}
{{Basic Page}}
==HTTP==

Hypertext Transfer Protocol (HTTP) is an application-layer protocol. HTTP is generally implemented on top of <tt><abbr title="Transmission Control Protocol, Internet Protocol"><nowiki>TCP/IP</nowiki></abbr></tt> default port 80, but can be implemented on any interface supporting a duplex stream. It is used for exchanging messages (such has hypermedia documents) in between a client (a ''user agent'' like a browser or bot) and a server. The interactions are defined by a client-server model. The client sends a request to a server and the server sends back a response to the client.

HTTP was one of the first protocols developed as part of Web starting in late 1989<ref>http://webfoundation.org/about/vision/history-of-the-web/</ref>, and later standardized over the course of many RFCs through the IETF.

* [[http/headers|List of HTTP headers]]
* [[http/methods|List of HTTP methods]]
* [[http/response status codes|List of HTTP status codes]]
* HTTP the protocol: The entity-body and transfer control, what are resources
* [[concepts/Internet and Web/how browsers work#The browser's high level structure|Layered requests]] with proxies and gateways
* [[http/requesting resources|Requesting resources]]: GET, HEAD, OPTIONS
* [[http/resource metadata|Resource metadata]]: Link, Last-Modified, Content-Type, Allow, etc
* [[http/caching|Caching]] and conditional requests
* [[http/access control|Access control]]
* [[http/state management|State management]] with cookies
* [[http/content negotiation|Content negotiation]]: Accept, Content-Location
* [[http/partial responses|Partial content responses]]
* [[http/modifying resources|Modification of resources]]: PUT, PATCH
* [[http/conditional updates|Conditional updates]]
* [[http/forms and scripts|Forms and scripts]]: POST with HTML Forms, using 3xx Status codes

=== An HTTP Request ===

HTTP is a plain-text protocol in the style of MIME (used by Email). An HTTP request begins with a client making a request to a server. The request contains a ''request-line'' identifying a [[http/methods|method]], the name of a resource, and the HTTP version of the request. This is followed by a number of [[http/headers|header lines]], then a blank line, and an optional request-body.

The server response is similar: It responds with the status-line consisting of the HTTP version, followed by a 3-digit numeric [[http/response status codes|status code]] and a status message. This is followed by a number of header lines, blank line, and optional response-body.

Lines are terminated with a carriage-return line-feed (CRLF, or "\r\n").

An example HTTP request will look like:

 GET / HTTP/1.1
 Host: example.com
 User-Agent: ExampleUA/4.0
 Accept: */*
 

To which the server might reply:


 HTTP/1.1 200 OK
 Date: Thu, 17 Jul 2014 15:08:35 GMT
 Expires: Fri, 18 Jul 2014 15:08:35 GMT
 Cache-Control: public
 Content-Type: text/plain;charset=UTF-8
 Server: ExampleServer/4.0
 Content-Length: 74
 
 Hypertext Transfer Protocol (HTTP) is an application-layer protocol. ...

Some of the most common headers include:

; Host : Provides the hostname for supporting multiple hostnames on a single server. For backwards compatibility, this is required even if the request is made in absolute form.
; User-Agent : A string identifying the version of software making the request
; Accept : Informs the server of which media-types the user agent would like to see, used for Content-Type negotiation
; Date : Indicates what date/time the message originated.  Required in responses.
; Expires : A caching header which indicates the time after which the resource will be "stale".
; Cache-Control : A caching header that can describe who is allowed to cache the resource and for how long
; Server : A string identifying the version of the server responding to the request
; Content-Type : Indicates the media type (MIME type) of the attached entity body, if any.
; Content-Length : Indicates the length of the attached entity body, if any.

=== Design of HTTP ===

HTTP follows a number of patterns to give it well-defined functionality for the benefit of clients and servers:

* it is ''client-server'', which separates data storage concerns from user interface concerns;
* it is ''layered'', to allow intermediate processing steps along the network path;
* it is ''stateless'', so server load is proportional with the number of requests instead of the total number of users; and
* it is ''cachable'', to enhance scalability and network performance.

=== History of HTTP ===

==== List of Specifications ====

# Informally implemented since 1991
# HTTP/1.0, May 1996 [http://tools.ietf.org/html/rfc1945 RFC1945]
# HTTP/1.1 first revision, January 1997 [http://tools.ietf.org/html/rfc2068 RFC2068]
# HTTP/1.1, second revision June 1999 [http://tools.ietf.org/html/rfc2616 RFC2616]
# HTTP/1.1, third revision June 2014 [http://tools.ietf.org/html/rfc7230 RFC7230] [http://tools.ietf.org/html/rfc7231 RFC7231] [http://tools.ietf.org/html/rfc7232 RFC7232] [http://tools.ietf.org/html/rfc7233 RFC7233] [http://tools.ietf.org/html/rfcC7234 RFC7234] [http://tools.ietf.org/html/rfcC7235 RFC7235]




== References ==
<references/>
{{Notes_Section}}
{{Topics|Web Services}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTTP
}}