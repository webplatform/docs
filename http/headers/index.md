
The full list of HTTP headers is shared with MIME headers and is maintained by the IANA at [http://www.iana.org/assignments/message-headers/message-headers.xhtml Message Headers]

== General Headers ==
{| class="wikitable"
|-
! Header !! Description !! Reference
|-
| Date || The date and time at which the message was originated || [http://tools.ietf.org/html/rfc7231#section-7.1.1.2 RFC7231 Section 7.1.1.2]
|}

== Request Headers ==
{| class="wikitable"
|-
! Header !! Description !! Reference
|-
| Accept || Lists Content-Types acceptable to the user agent || [http://tools.ietf.org/html/rfc7231#section-5.3.2 RFC7231 Section 5.3.2]
|}

== Response Headers ==
{| class="wikitable"
|-
! Header !! Description !! Reference
|-
| Server || Lists the server's software version || [http://tools.ietf.org/html/rfc7231#section-7.4.2 RFC7231 Section 7.4.2]
|-
|}


== Headers by Function ==

=== Informational ===
* User-Agent
* Server
* From
* Date
* Referer [sic]

=== Resource Metadata ===
* Content-Location
* Link
* Last-Modified
* ETag
* Content-MD5
* Allow

=== Transfer Control ===
* Transfer-Encoding
* Content-Length
* Expect: 100-continue

=== Entity Body and Partial Content ===
* Content-Range
* Accept-Ranges
* If-Range
* Range

=== Caching ===
* Expires
* Date
* Age
* Cache-Control
* ETag
* Last-Modified
* Content-Location

=== Conditional Requests ===
* If-Modified-Since
* If-Match
* If-Unmodified-Since
* If-None-Match
* If-Range
* ETag
* Last-Modified

=== Authentication ===
* WWW-Authenticate
* Authorization
* Proxy-Authenticate
* Proxy-Authorization

=== Content-Type Negotiation ===
* Accept
* Accept-Charset
* Accept-Language
* Accept-Ranges

== Crafting New Headers ==
See [http://tools.ietf.org/html/rfc7231#section-8.3.1 RFC7231 Section 8.3.1].

If the response is identifying another resource, use the Link header with a URI as the relation name, e.g.:

 <nowiki>Link: <http://example.com/AcmeMetals>;rel="http://example.com/coin-minted-by"</nowiki>