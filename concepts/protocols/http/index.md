---
title: http
tags:
  - Basic
  - Pages
  - Web
  - Services
readiness: 'Not Ready'
summary: 'HTTP is an application-layer protocol used for storing, retrieving, and communicating about information resources on a remote server. It is the transfer protocol used by the Web, and defines many features to support caching, authentication, manipulation of resources, negotiation of functionality, and more.'
uri: concepts/protocols/http
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'http/requesting resources'
    - 'http/resource metadata'
    - http/caching
    - 'http/access control'
    - 'http/state management'
    - 'http/content negotiation'
    - 'http/partial responses'
    - 'http/modifying resources'
    - 'http/conditional updates'
    - 'http/forms and scripts'

---
# HTTP

## Summary

HTTP is an application-layer protocol used for storing, retrieving, and communicating about information resources on a remote server. It is the transfer protocol used by the Web, and defines many features to support caching, authentication, manipulation of resources, negotiation of functionality, and more.

## HTTP

Hypertext Transfer Protocol (HTTP) is an application-layer protocol. HTTP is generally implemented on top of `TCP/IP` default port 80, but can be implemented on any interface supporting a duplex stream. It is used for exchanging messages (such has hypermedia documents) in between a client (a *user agent* like a browser or bot) and a server. The interactions are defined by a client-server model. The client sends a request to a server and the server sends back a response to the client.

HTTP was one of the first protocols developed as part of Web starting in late 1989<sup>[[1]](#cite_note-1)</sup>, and later standardized over the course of many RFCs through the IETF.

-   [List of HTTP headers](/http/headers)
-   [List of HTTP methods](/http/methods)
-   [List of HTTP status codes](/http/response_status_codes)
-   HTTP the protocol: The entity-body and transfer control, what are resources
-   [Layered requests](/concepts/Internet_and_Web/how_browsers_work#The_browser.27s_high_level_structure) with proxies and gateways
-   [Requesting resources](/w/index.php?title=http/requesting_resources&action=edit&redlink=1): GET, HEAD, OPTIONS
-   [Resource metadata](/w/index.php?title=http/resource_metadata&action=edit&redlink=1): Link, Last-Modified, Content-Type, Allow, etc
-   [Caching](/w/index.php?title=http/caching&action=edit&redlink=1) and conditional requests
-   [Access control](/w/index.php?title=http/access_control&action=edit&redlink=1)
-   [State management](/w/index.php?title=http/state_management&action=edit&redlink=1) with cookies
-   [Content negotiation](/w/index.php?title=http/content_negotiation&action=edit&redlink=1): Accept, Content-Location
-   [Partial content responses](/w/index.php?title=http/partial_responses&action=edit&redlink=1)
-   [Modification of resources](/w/index.php?title=http/modifying_resources&action=edit&redlink=1): PUT, PATCH
-   [Conditional updates](/w/index.php?title=http/conditional_updates&action=edit&redlink=1)
-   [Forms and scripts](/w/index.php?title=http/forms_and_scripts&action=edit&redlink=1): POST with HTML Forms, using 3xx Status codes

### An HTTP Request

HTTP is a plain-text protocol in the style of MIME (used by Email). An HTTP request begins with a client making a request to a server. The request contains a *request-line* identifying a [method](/http/methods), the name of a resource, and the HTTP version of the request. This is followed by a number of [header lines](/http/headers), then a blank line, and an optional request-body.

The server response is similar: It responds with the status-line consisting of the HTTP version, followed by a 3-digit numeric [status code](/http/response_status_codes) and a status message. This is followed by a number of header lines, blank line, and optional response-body.

Lines are terminated with a carriage-return line-feed (CRLF, or "\\r\\n").

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

 HostÂ
:   Provides the hostname for supporting multiple hostnames on a single server. For backwards compatibility, this is required even if the request is made in absolute form.
 User-AgentÂ
:   A string identifying the version of software making the request
 AcceptÂ
:   Informs the server of which media-types the user agent would like to see, used for Content-Type negotiation
 DateÂ
:   Indicates what date/time the message originated. Required in responses.
 ExpiresÂ
:   A caching header which indicates the time after which the resource will be "stale".
 Cache-ControlÂ
:   A caching header that can describe who is allowed to cache the resource and for how long
 ServerÂ
:   A string identifying the version of the server responding to the request
 Content-TypeÂ
:   Indicates the media type (MIME type) of the attached entity body, if any.
 Content-LengthÂ
:   Indicates the length of the attached entity body, if any.

### Design of HTTP

HTTP follows a number of patterns to give it well-defined functionality for the benefit of clients and servers:

-   it is *client-server*, which separates data storage concerns from user interface concerns;
-   it is *layered*, to allow intermediate processing steps along the network path;
-   it is *stateless*, so server load is proportional with the number of requests instead of the total number of users; and
-   it is *cachable*, to enhance scalability and network performance.

### History of HTTP

#### List of Specifications

1.  Informally implemented since 1991
2.  HTTP/1.0, May 1996 [RFC1945](http://tools.ietf.org/html/rfc1945)
3.  HTTP/1.1 first revision, January 1997 [RFC2068](http://tools.ietf.org/html/rfc2068)
4.  HTTP/1.1, second revision June 1999 [RFC2616](http://tools.ietf.org/html/rfc2616)
5.  HTTP/1.1, third revision June 2014 [RFC7230](http://tools.ietf.org/html/rfc7230) [RFC7231](http://tools.ietf.org/html/rfc7231) [RFC7232](http://tools.ietf.org/html/rfc7232) [RFC7233](http://tools.ietf.org/html/rfc7233) [RFC7234](http://tools.ietf.org/html/rfcC7234) [RFC7235](http://tools.ietf.org/html/rfcC7235)

## References

1.  <span class="mw-cite-backlink">[â†‘](#cite_ref-1)</span> <span class="reference-text">[http://webfoundation.org/about/vision/history-of-the-web/](http://webfoundation.org/about/vision/history-of-the-web/)</span>

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTTP)

