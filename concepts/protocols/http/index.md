{{Page_Title|HTTP}}
{{Flags
|State=Not Ready
|Checked_Out=No
|High-level issues=Stub, Missing Relevant Sections
}}
{{Summary_Section|HTTP is an application-layer protocol used for storing, retrieving, and communicating about information resources on a remote server. It is the transfer protocol used by the Web, and defines many features to support caching, authentication, manipulation of resources, negotiation of functionality, and more.}}
{{Basic Page}}
==HTTP==

The Hypertext Transfer Protocol (HTTP) is an application-layer protocol. HTTP is an application-level protocol on top of [[TCP/IP]], a communication protocol. It is used for exchanging messages (such has hypermedia documents) in between a client (a ''user agent'' like a browser or bot) and a server. The interactions are defined by a client-server model. The client sends a request to a server and the server sends back a response to the client.

HTTP will help manage an information space by defining user interactions and expectations with regards to this information.

=== History of HTTP ===

==== List of Specifications ====

# HTTP/1.0, May 1996 RFC1945
# HTTP/1.1 first revision, January 1997 RFC2068
# HTTP/1.1, second revision June 1999 RFC2616
# HTTP/1.1, third revision June 2014 RFC7230 RFC7231 RFC7232 RFC7233 RFC7234 RFC7235

=== An HTTP Request ===

HTTP is a plain-text protocol in the style of MIME (used by Email). An HTTP request begins with a client making a request to a server. The request contains a ''request-line'' identifying a [[http/methods|method]], the name of a resource, and the HTTP version of the request. This is followed by a number of header lines, then a blank line, and an optional request-body.

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
    Content-Type: text/plain; charset=UTF-8
    Server: ExampleServer/4.0
    Transfer-Encoding: chunked
    
    Welcome to our server!

=== Design of HTTP ===

HTTP follows a number of patterns to give it well-defined functionality for the benefit of clients and servers:

* it is ''client-server'', which separates data storage concerns from user interface concerns;
* it is ''layered'', to allow intermediate processing steps along the network path;
* it is ''stateless'', so server load is proportional with the number of requests instead of the total number of users; and
* it is ''cachable'', to enhance scalability and network performance.
{{Notes_Section}}
{{Topics|Web Services}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTTP
|MSDN_link=
|HTML5Rocks_link=
}}