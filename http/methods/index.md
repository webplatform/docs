[[concepts/protocols/http|HTTP]] is a stateless application level protocol. An HTTP client constructs requests [[messages]] to communicate specific intentions. The '''method''' token indicates the purpose for which the client has made this request.

Associating the method with compatible [[http/headers|HTTP headers]], a client may further specialize the request to the server. It may trigger different answers from the server.

The HTTP/1.1 Specification defines a number of [http://tools.ietf.org/html/rfc7231#section-4.1 standardized methods]. Some other methods are standardized in different documents.

== Standardized Methods ==

The minimum requirement for [[http/servers|HTTP servers]] is to support the methods GET and HEAD.

=== GET ===
GET requests an information resource from the HTTP server. A GET request "safe": it is read only, and must not change the state of the server (except to the extent the very act of the request is logged, etc).

A GET request can be paired with an <code>If-Match</code> header if the user agent has a cached version with an ETag value, and only wishes for a response if there's a newer version available.

=== HEAD ===
A HEAD request is identical to a GET request, except the response body is excluded. It is used for testing headers and metadata about a resource.

=== POST ===
POST is used to execute a script on the server. The result might be to e.g. make a purchase of an item, and so is not safe to re-make.

If specified in the response, POST requests are cachable.

Most POST requests are made by Web browsers, and respond with 303 (See Other) to redirect the browser to the modified resource, or some form of landing page, after successful execution.

=== PUT ===
PUT stores a resource at the given URI, creating it if necessary.

Two PUT requests in succession have the same effect as one, so the method is _idempotent_ (safe to re-send). PUT requests should be sent with an <code>If-Match: ''etag''</code> so modifications are not inadvertently overwritten; or <code>If-None-Match: *</code> if the resource is to only be created (but not overwritten if it exists).

=== DELETE ===
A DELETE on a resource removes it from the server. Further GET requests will likely return 410 (Gone) or 404 (Not Found).

Like PUT, two DELETE requests in succession have the same effect as one, and so the method is _idempotent_ (safe to re-send). DELETE requests should be paired with an <code>If-Match</code> header so that if the resource is re-created or modified, the modifications are not unknowingly deleted.

=== CONNECT ===
CONNECT effectively ends HTTP communications and starts two-way communications with the resource identified in the request-line (the URI, or server:port). It is a hop-by-hop method.

=== OPTIONS ===
An OPTIONS request on a resource requests information about that resource.

OPTIONS is required by CORS to enable cross-domain [[apis/xhr|XMLHttpRequest]] requests.

=== TRACE ===
TRACE is a meta-request that replies with the HTTP headers used to make the request. It is defined primarily for debugging.

TRACE in many situations can expose confidential cookie and authorization headers to an attacker, and so is disabled on many HTTP servers. See [http://www.kb.cert.org/vuls/id/867593].

=== Other Methods ===
Several HTTP extensions like WebDAV define other methods. A complete list is maintained at the IANA's [http://www.iana.org/assignments/http-methods/http-methods.xhtml HTTP Method Registry].

== Method Properties ==

@@TODO: add something about safe, idempotent and cacheable. Probably make a table@@

{| class="wikitable"
|-
! Method !! Summary !! Safe !! Idempotent !! Cachable !! Reference
|-
| GET || Retrieve a resource || Yes || Yes || Yes || [http://tools.ietf.org/html/rfc7231#section-4.3.1 RFC7231, Section 4.3.1]
|-
| HEAD || As GET, but headers only || Yes || Yes || Yes || [http://tools.ietf.org/html/rfc7231#section-4.3.2 RFC7231, Section 4.3.2]
|-
| POST || Execute/perform an action || No || No || Yes || [http://tools.ietf.org/html/rfc7231#section-4.3.3 RFC7231, Section 4.3.3]
|-
| PUT || Store a resource || No || Yes || No || [http://tools.ietf.org/html/rfc7231#section-4.3.4 RFC7231, Section 4.3.4]
|-
| DELETE || Delete a resource || No || Yes || No || [http://tools.ietf.org/html/rfc7231#section-4.3.6 RFC7231, Section 4.3.6]
|-
| CONNECT || Open a tunnel || No || No || No || [http://tools.ietf.org/html/rfc7231#section-4.3.6 RFC7231, Section 4.3.6]
|-
| OPTIONS || Get communication information || No || Yes || No || [http://tools.ietf.org/html/rfc7231#section-4.3.7 RFC7231, Section 4.3.7]
|}