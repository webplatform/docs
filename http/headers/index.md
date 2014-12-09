
The full list of HTTP headers is shared with MIME headers and is maintained by the IANA at [http://www.iana.org/assignments/message-headers/message-headers.xhtml Message Headers]

== Headers by Function ==

=== Informational ===
* Main article: [[http/requesting resources|Requesting resources]]: GET, HEAD, OPTIONS
* Main article: [[http/modifying resources|Modification of resources]]: PUT, PATCH
* Main article: [[http/forms and scripts|Forms and scripts]]: POST with HTML Forms, using 3xx Status codes
* [[http/headers/User-Agent|User-Agent]]
* [[http/headers/Server|Server]]
* [[http/headers/From|From]]
* [[http/headers/Date|Date]]
* [[http/headers/Referer|Referer]] [sic]

=== Resource Metadata ===
* Main article: [[http/resource metadata|Resource metadata]]: Link, Last-Modified, Content-Type, Allow, etc
* [[http/headers/Content-Location|Content-Location]]
* [[http/headers/Link|Link]]
* [[http/headers/Last-Modified|Last-Modified]]
* [[http/headers/ETag|ETag]]
* [[http/headers/Content-MD5|Content-MD5]]
* [[http/headers/Allow|Allow]]

=== Transfer Control ===
* Main article: [[http/requesting resources|Requesting resources]]: GET, HEAD, OPTIONS
* [[http/headers/Transfer-Encoding|Transfer-Encoding]]
* [[http/headers/Content-Length|Content-Length]]
* [[http/headers/Expect|Expect]]: 100-continue

=== Entity Body and Partial Content ===
* Main article: [[http/partial responses|Partial content responses]]
* [[http/headers/Content-Range|Content-Range]]
* [[http/headers/Accept-Ranges|Accept-Ranges]]
* [[http/headers/If-Range|If-Range]]
* [[http/headers/Range|Range]]

=== Caching ===
* Main article: [[http/layered requests|Layered requests]] with proxies and gateways
* [[http/headers/Expires|Expires]]
* [[http/headers/Date|Date]]
* [[http/headers/Age|Age]]
* [[http/headers/Cache-Control|Cache-Control]]
* [[http/headers/ETag|ETag]]
* [[http/headers/Last-Modified|Last-Modified]]
* [[http/headers/Content-Location|Content-Location]]

=== Conditional Requests ===
* Main article: [[http/caching|Caching]] and conditional requests
* Main article: [[http/conditional updates|Conditional updates]]
* [[http/headers/If-Modified-Since|If-Modified-Since]]
* [[http/headers/If-Match|If-Match]]
* [[http/headers/If-Unmodified-Since|If-Unmodified-Since]]
* [[http/headers/If-None-Match|If-None-Match]]
* [[http/headers/If-Range|If-Range]]
* [[http/headers/ETag|ETag]]
* [[http/headers/Last-Modified|Last-Modified]]

=== Authentication and Access Control ===
* Main article: [[http/access control|Access control]]
* [[http/headers/WWW-Authenticate|WWW-Authenticate]]
* [[http/headers/Authorization|Authorization]]
* [[http/headers/Proxy-Authenticate|Proxy-Authenticate]]
* [[http/headers/Proxy-Authorization|Proxy-Authorization]]

=== Content-Type Negotiation ===
* Main article: [[http/content negotiation|Content negotiation]]: Accept, Content-Location
* [[http/headers/Accept|Accept]]
* [[http/headers/Accept-Charset|Accept-Charset]]
* [[http/headers/Accept-Language|Accept-Language]]
* [[http/headers/Accept-Ranges|Accept-Ranges]]

== Crafting New Headers ==
See [http://tools.ietf.org/html/rfc7231#section-8.3.1 RFC7231 Section 8.3.1].

If the response is identifying another resource, use the Link header with a URI as the relation name, e.g.:

 <nowiki>Link: <http://example.com/AcmeMetals>;rel="http://example.com/coin-minted-by"</nowiki>

== Table of Headers ==
{| class="wikitable"
|-
! Header !! Description !! Reference
|-
| [[http/headers/A-IM|A-IM]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Accept|Accept]]
| 
| [http://tools.ietf.org/html/rfc7231#section-5.3.2 RFC7231, Section 5.3.2]
|-
| [[http/headers/Accept-Additions|Accept-Additions]]
| Used in Hyper Text Coffee Pot Control Protocol (HTCPCP/1.0)
| [http://tools.ietf.org/html/rfc2324#section-2.2.2.1 RFC2324]
|-
| [[http/headers/Accept-Charset|Accept-Charset]]
| 
| [http://tools.ietf.org/html/rfc7231#section-5.3.3 RFC7231, Section 5.3.3]
|-
| [[http/headers/Accept-Datetime|Accept-Datetime]]
| 
| [http://tools.ietf.org/html/rfc7089 RFC7089]
|-
| [[http/headers/Accept-Encoding|Accept-Encoding]]
| 
| [http://tools.ietf.org/html/rfc7231#section-5.3.4 RFC7231, Section 5.3.4]
|-
| [[http/headers/Accept-Features|Accept-Features]]
| Experimental
| [http://tools.ietf.org/html/rfc2295#section-8.2 RFC2995]
|-
| [[http/headers/Accept-Language|Accept-Language]]
| Locales that a user agent prefers
| [http://tools.ietf.org/html/rfc7231#section-5.3.5 RFC7231, Section 5.3.5]
|-
| [[http/headers/Accept-Patch|Accept-Patch]]
| Specifies media types that are acceptable for PATCH requests
| [http://tools.ietf.org/html/rfc5789 RFC5789]
|-
| [[http/headers/Accept-Ranges|Accept-Ranges]]
| Server indication of which range units it understands (e.g. byte)
| [http://tools.ietf.org/html/rfc7233#section-2.3 RFC7233, Section 2.3]
|-
| [[http/headers/Age|Age]]
| Estimate of how stale the resource is, in seconds, used by caches
| [http://tools.ietf.org/html/rfc7234#section-5.1 RFC7234, Section 5.1]
|-
| [[http/headers/Allow|Allow]]
| Indicate which methods can be used on the resource
| [http://tools.ietf.org/html/rfc7231#section-7.4.1 RFC7231, Section 7.4.1]
|-
| [[http/headers/Alternates|Alternates]]
| Experimental
| [http://tools.ietf.org/html/rfc2295 RFC2295]
|-
| [[http/headers/Apply-To-Redirect-Ref|Apply-To-Redirect-Ref]]
| 
| [http://tools.ietf.org/html/rfc4437 RFC4437]
|-
| [[http/headers/Authentication-Info|Authentication-Info]]
| Control data and information about the authentication session
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Authorization|Authorization]]
| Credentials for accessing a resource on the server
| [http://tools.ietf.org/html/rfc7235#section-4.2 RFC7235, Section 4.2]
|-
| [[http/headers/Cache-Control|Cache-Control]]
| Information for how and when to cache the resource
| [http://tools.ietf.org/html/rfc7234#section-5.2 RFC7234, Section 5.2]
|-
| [[http/headers/Close|Close]]
| Not actually a valid header. Reserved to prevent conflicts with [[http/headers/Connection|<code>Connection</code>]]<code>: close</code>
| [http://tools.ietf.org/html/rfc7230#section-8.1 RFC7230, Section 8.1]
|-
| [[http/headers/Connection|Connection]]
| 
| [http://tools.ietf.org/html/rfc7230#section-6.1 RFC7230, Section 6.1]
|-
| [[http/headers/Content-Base|Content-Base]]
| Provides a base URI for the document (largely unsupported and obsolete)
| [http://tools.ietf.org/html/rfc2068 RFC2068][http://www.iana.org/go/rfc2616 RFC2616]
|-
| [[http/headers/Content-Disposition|Content-Disposition]]
| Conveys additional information about how to process the response payload
| [http://tools.ietf.org/html/rfc6266 RFC6266]
|-
| [[http/headers/Content-Encoding|Content-Encoding]]
| See also [[http/headers/Transfer-Encoding|Transfer-Encoding]]
| [http://tools.ietf.org/html/rfc7231#section-3.1.2.2 RFC7231, Section 3.1.2.2]
|-
| [[http/headers/Content-ID|Content-ID]]
| Obsolete
| [http://tools.ietf.org/html/rfc4229 RFC4229] [http://www.w3.org/TR/NOTE-drp-19970825 DRP]
|-
| [[http/headers/Content-Language|Content-Language]]
| The locale/language of the entity-body
| [http://tools.ietf.org/html/rfc7231#section-3.1.3.2 RFC7231, Section 3.1.3.2]
|-
| [[http/headers/Content-Length|Content-Length]]
| The octet (byte) length of the attached entity-body
| [http://tools.ietf.org/html/rfc7230#section-3.3.2 RFC7230, Section 3.3.2]
|-
| [[http/headers/Content-Location|Content-Location]]
| The URI of the attached entity-body
| [http://tools.ietf.org/html/rfc7231#section-3.1.4.2 RFC7231, Section 3.1.4.2]
|-
| [[http/headers/Content-MD5|Content-MD5]]
| Obsolete
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Content-Range|Content-Range]]
| Identifies the enclose entity-body is a subset of the requested resource
| [http://tools.ietf.org/html/rfc7233#section-4.2 RFC7233, Section 4.2]
|-
| [[http/headers/Content-Script-Type|Content-Script-Type]]
| 
| [http://www.w3.org/TR/html401/interact/scripts.html#h-18.2.2 HTML 4.01 Section 18.2.2]
|-
| [[http/headers/Content-Style-Type|Content-Style-Type]]
| 
| [http://www.w3.org/TR/html401/present/styles.html#h-14.2.1 HTML 4.01 Section 14.2.1]
|-
| [[http/headers/Content-Type|Content-Type]]
| The media type of the attached entity-body
| [http://tools.ietf.org/html/rfc7231#section-3.1.1.5 RFC7231, Section 3.1.1.5]
|-
| [[http/headers/Content-Version|Content-Version]]
| Obsolete
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Cookie|Cookie]]
| Declares a stored cookie value to the server
| [http://tools.ietf.org/html/rfc6265 RFC6265]
|-
| [[http/headers/Cookie2|Cookie2]]
| Declares a stored cookie value to the server; Obsolete
| [http://tools.ietf.org/html/rfc2965 RFC2965][http://www.iana.org/go/rfc6265 RFC6265]
|-
| [[http/headers/DASL|DASL]]
| 
| [http://tools.ietf.org/html/rfc5323 RFC5323]
|-
| [[http/headers/DAV|DAV]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4918 RFC4918]
|-
| [[http/headers/Date|Date]]
| The date and time at which the message was originated
| [http://tools.ietf.org/html/rfc7231#section-7.1.1.2 RFC7231, Section 7.1.1.2]
|-
| [[http/headers/Default-Style|Default-Style]]
| 
| [http://www.w3.org/TR/html401/present/styles.html#h-14.3.2 HTML 4.01 Section 14.3.2]
|-
| [[http/headers/Delta-Base|Delta-Base]]
| The entity tag of the base instance against which the delta applies
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Depth|Depth]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4918 RFC4918]
|-
| [[http/headers/Derived-From|Derived-From]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Destination|Destination]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4918 RFC4918]
|-
| [[http/headers/Differential-ID|Differential-ID]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Digest|Digest]]
| Indicates a hash/digest for the full resource
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/ETag|ETag]]
| Differentiates between multiple versions/representations of the same resource
| [http://tools.ietf.org/html/rfc7232#section-2.3 RFC7232, Section 2.3]
|-
| [[http/headers/Expect|Expect]]
| Require that downstream nodes support specified functionality
| [http://tools.ietf.org/html/rfc7231#section-5.1.1 RFC7231, Section 5.1.1]
|-
| [[http/headers/Expires|Expires]]
| Controls caching
| [http://tools.ietf.org/html/rfc7234#section-5.3 RFC7234, Section 5.3]
|-
| [[http/headers/Ext|Ext]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Forwarded|Forwarded]]
| Shows where the message originated from, further upstream
| [http://tools.ietf.org/html/rfc7239 RFC7239]
|-
| [[http/headers/From|From]]
| Contact information for the user making the request, especially for Web spiders
| [http://tools.ietf.org/html/rfc7231#section-5.5.1 RFC7231, Section 5.5.1]
|-
| [[http/headers/Host|Host]]
| Hostname component of the request-URI (Required)
| [http://tools.ietf.org/html/rfc7230#section-5.4 RFC7230, Section 5.4]
|-
| [[http/headers/IM|IM]]
| Instance Manipulation
| [http://tools.ietf.org/html/rfc4229 RFC4229] [http://tools.ietf.org/html/rfc3229#section-10.5.2 RFC 3229]
|-
| [[http/headers/If|If]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4918 RFC4918]
|-
| [[http/headers/If-Match|If-Match]]
| Conditional request header
| [http://tools.ietf.org/html/rfc7232#section-3.1 RFC7232, Section 3.1]
|-
| [[http/headers/If-Modified-Since|If-Modified-Since]]
| Conditional request header
| [http://tools.ietf.org/html/rfc7232#section-3.3 RFC7232, Section 3.3]
|-
| [[http/headers/If-None-Match|If-None-Match]]
| Conditional request header
| [http://tools.ietf.org/html/rfc7232#section-3.2 RFC7232, Section 3.2]
|-
| [[http/headers/If-Range|If-Range]]
| Conditional request header
| [http://tools.ietf.org/html/rfc7233#section-3.2 RFC7233, Section 3.2]
|-
| [[http/headers/If-Schedule-Tag-Match|If-Schedule-Tag-Match]]
| Part of Scheduling Extensions to CalDAV
| [http://tools.ietf.org/html/rfc6638 RFC6638]
|-
| [[http/headers/If-Unmodified-Since|If-Unmodified-Since]]
| Conditional request header
| [http://tools.ietf.org/html/rfc7232#section-3.4 RFC7232, Section 3.4]
|-
| [[http/headers/Keep-Alive|Keep-Alive]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Label|Label]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Last-Modified|Last-Modified]]
| 
| [http://tools.ietf.org/html/rfc7232#section-2.2 RFC7232, Section 2.2]
|-
| [[http/headers/Link|Link]]
| Declares a link relationship to another resource
| [http://tools.ietf.org/html/rfc5988 RFC5988]
|-
| [[http/headers/Location|Location]]
| Points to another resource, typically for redirection purposes
| [http://tools.ietf.org/html/rfc7231#section-7.1.2 RFC7231, Section 7.1.2]
|-
| [[http/headers/Lock-Token|Lock-Token]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4918 RFC4918]
|-
| [[http/headers/Man|Man]]
| Experimental
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Max-Forwards|Max-Forwards]]
| Limit the number of forwards, similar to a TTL
| [http://tools.ietf.org/html/rfc7231#section-5.1.2 RFC7231, Section 5.1.2]
|-
| [[http/headers/Memento-Datetime|Memento-Datetime]]
| 
| [http://tools.ietf.org/html/rfc7089 RFC7089]
|-
| [[http/headers/Meter|Meter]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229] [http://tools.ietf.org/html/rfc2227 RFC2227]
|-
| [[http/headers/MIME-Version|MIME-Version]]
| The HTTP Message is also MIME compatible (obsolete)
| [http://tools.ietf.org/html/rfc7231#appendix-A.1 RFC7231, Appendix A.1]
|-
| [[http/headers/Negotiate|Negotiate]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229] [http://tools.ietf.org/html/rfc2295 RFC2295]
|-
| [[http/headers/Opt|Opt]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Ordering-Type|Ordering-Type]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Origin|Origin]]
| 
| [http://tools.ietf.org/html/rfc6454 RFC6454]
|-
| [[http/headers/Overwrite|Overwrite]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4918 RFC4918]
|-
| [[http/headers/P3P|P3P]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/PEP|PEP]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/PICS-Label|PICS-Label]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Pep-Info|Pep-Info]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Position|Position]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Pragma|Pragma]]
| (Deprecated HTTP/1.0 header)
| [http://tools.ietf.org/html/rfc7234#section-5.4 RFC7234, Section 5.4]
|-
| [[http/headers/Prefer|Prefer]]
| Indicate a preference for how the server should respond to a query
| [http://tools.ietf.org/html/rfc7240 RFC7240]
|-
| [[http/headers/Preference-Applied|Preference-Applied]]
| 
| [http://tools.ietf.org/html/rfc7240 RFC7240]
|-
| [[http/headers/ProfileObject|ProfileObject]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Proxy-Authenticate|Proxy-Authenticate]]
| Use of proxy requires authentication
| [http://tools.ietf.org/html/rfc7235#section-4.3 RFC7235, Section 4.3]
|-
| [[http/headers/Proxy-Authentication-Info|Proxy-Authentication-Info]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Proxy-Authorization|Proxy-Authorization]]
| Send credentials to a proxy
| [http://tools.ietf.org/html/rfc7235#section-4.4 RFC7235, Section 4.4]
|-
| [[http/headers/Proxy-Features|Proxy-Features]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Proxy-Instruction|Proxy-Instruction]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Public|Public]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Range|Range]]
| Request a subset of the resource
| [http://tools.ietf.org/html/rfc7233#section-3.1 RFC7233, Section 3.1]
|-
| [[http/headers/Redirect-Ref|Redirect-Ref]]
| 
| [http://tools.ietf.org/html/rfc4437 RFC4437]
|-
| [[http/headers/Referer|Referer]]
| (Sic) Page that was linked from
| [http://tools.ietf.org/html/rfc7231#section-5.5.2 RFC7231, Section 5.5.2]
|-
| [[http/headers/Retry-After|Retry-After]]
| 
| [http://tools.ietf.org/html/rfc7231#section-7.1.3 RFC7231, Section 7.1.3]
|-
| [[http/headers/Safe|Safe]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Schedule-Reply|Schedule-Reply]]
| Part of Scheduling Extensions to CalDAV
| [http://tools.ietf.org/html/rfc6638 RFC6638]
|-
| [[http/headers/Schedule-Tag|Schedule-Tag]]
| Part of Scheduling Extensions to CalDAV
| [http://tools.ietf.org/html/rfc6638 RFC6638]
|-
| [[http/headers/Sec-WebSocket-Accept|Sec-WebSocket-Accept]]
| Used for negotiating a WebSocket connection
| [http://tools.ietf.org/html/rfc6455 RFC6455]
|-
| [[http/headers/Sec-WebSocket-Extensions|Sec-WebSocket-Extensions]]
| Used for negotiating a WebSocket connection
| [http://tools.ietf.org/html/rfc6455 RFC6455]
|-
| [[http/headers/Sec-WebSocket-Key|Sec-WebSocket-Key]]
| Used for negotiating a WebSocket connection
| [http://tools.ietf.org/html/rfc6455 RFC6455]
|-
| [[http/headers/Sec-WebSocket-Protocol|Sec-WebSocket-Protocol]]
| Used for negotiating a WebSocket connection
| [http://tools.ietf.org/html/rfc6455 RFC6455]
|-
| [[http/headers/Sec-WebSocket-Version|Sec-WebSocket-Version]]
| Used for negotiating a WebSocket connection
| [http://tools.ietf.org/html/rfc6455 RFC6455]
|-
| [[http/headers/Security-Scheme|Security-Scheme]]
| Used to indicate S-HTTP support (not to be confused with HTTPS)
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Server|Server]]
| Indicates the server's software and version
| [http://tools.ietf.org/html/rfc7231#section-7.4.2 RFC7231, Section 7.4.2]
|-
| [[http/headers/Set-Cookie|Set-Cookie]]
| Request to store a cookie on the user-agent
| [http://tools.ietf.org/html/rfc6265 RFC6265]
|-
| [[http/headers/Set-Cookie2|Set-Cookie2]]
| Request to store a cookie on the user-agent; Obsolete
| [http://tools.ietf.org/html/rfc2965 RFC2965][http://www.iana.org/go/rfc6265 RFC6265]
|-
| [[http/headers/Slug|Slug]]
| Specifies a "slug" string to be used in the generation of URLs of new resources. Used by the Atom Publishing Protocol.
| [http://tools.ietf.org/html/rfc5023 RFC5023]
|-
| [[http/headers/SoapAction|SoapAction]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Status-URI|Status-URI]]
| Used by WebDAV
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Strict-Transport-Security|Strict-Transport-Security]]
| HSTS, asks that future requests must only go over TLS
| [http://tools.ietf.org/html/rfc6797 RFC6797]
|-
| [[http/headers/Surrogate-Capability|Surrogate-Capability]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Surrogate-Control|Surrogate-Control]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/TCN|TCN]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/TE|TE]]
| 
| [http://tools.ietf.org/html/rfc7230#section-4.3 RFC7230, Section 4.3]
|-
| [[http/headers/Timeout|Timeout]]
| Used in WebDAV
| [http://tools.ietf.org/html/rfc4918 RFC4918]
|-
| [[http/headers/Trailer|Trailer]]
| 
| [http://tools.ietf.org/html/rfc7230#section-4.4 RFC7230, Section 4.4]
|-
| [[http/headers/Transfer-Encoding|Transfer-Encoding]]
| Specifies how the payload has been compressed. See also [[http/headers/Content-Encoding|Content-Encoding]]
| [http://tools.ietf.org/html/rfc7230#section-3.3.1 RFC7230, Section 3.3.1]
|-
| [[http/headers/URI|URI]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Upgrade|Upgrade]]
| 
| [http://tools.ietf.org/html/rfc7230#section-6.7 RFC7230, Section 6.7]
|-
| [[http/headers/User-Agent|User-Agent]]
| Indicates the user agent's software and version
| [http://tools.ietf.org/html/rfc7231#section-5.5.3 RFC7231, Section 5.5.3]
|-
| [[http/headers/Variant-Vary|Variant-Vary]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Vary|Vary]]
| The server's response was chosen based on the specified headers
| [http://tools.ietf.org/html/rfc7231#section-7.1.4 RFC7231, Section 7.1.4]
|-
| [[http/headers/Via|Via]]
| 
| [http://tools.ietf.org/html/rfc7230#section-5.7.1 RFC7230, Section 5.7.1]
|-
| [[http/headers/WWW-Authenticate|WWW-Authenticate]]
| 
| [http://tools.ietf.org/html/rfc7235#section-4.1 RFC7235, Section 4.1]
|-
| [[http/headers/Want-Digest|Want-Digest]]
| 
| [http://tools.ietf.org/html/rfc4229 RFC4229]
|-
| [[http/headers/Warning|Warning]]
| 
| [http://tools.ietf.org/html/rfc7234#section-5.5 RFC7234, Section 5.5]
|-
| [[http/headers/X-Frame-Options|X-Frame-Options]]
| Older variation on Frame-Options header
| [http://tools.ietf.org/html/rfc7034 RFC7034] [http://www.w3.org/TR/CSP11/ CSP]
|}