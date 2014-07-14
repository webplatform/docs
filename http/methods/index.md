[[concepts/protocols/http|HTTP]] is a stateless application level protocol. An HTTP client constructs requests [[messages]] to communicate specific intentions. The '''method''' token indicates the purpose for which the client has made this request.

Associating the method with compatible [[http/headers|HTTP headers]], a client may further specialize the request to the server. It may trigger different answers from the server.

The HTTP/1.1 Specification defines a number of [http://tools.ietf.org/html/rfc7231#section-4.1 standardized methods]. Some other methods are standardized in different documents.

== Standardized Methods ==

The minimum requirement for [[http/servers|HTTP servers]] is to support the methods GET and HEAD.
=== GET ===
=== HEAD ===
=== POST ===
=== PUT ===
=== DELETE ===
=== CONNECT ===
=== OPTIONS ===
=== TRACE ===

== Method Properties ==

@@TODO: add something about safe, idempotent and cacheable. Probably make a table@@