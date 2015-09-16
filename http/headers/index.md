---
title: headers
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'http/requesting resources'
    - 'http/modifying resources'
    - 'http/forms and scripts'
    - 'http/resource metadata'
    - http/headers/Content-MD5
    - http/headers/Transfer-Encoding
    - http/headers/Content-Length
    - http/headers/Expect
    - 'http/partial responses'
    - http/headers/Content-Range
    - http/headers/Accept-Ranges
    - 'http/layered requests'
    - http/headers/Age
    - http/caching
    - 'http/conditional updates'
    - 'http/access control'
    - http/headers/WWW-Authenticate
    - http/headers/Proxy-Authenticate
    - http/headers/Proxy-Authorization
    - 'http/content negotiation'
    - http/headers/Accept-Charset
    - http/headers/Accept-Language
    - http/headers/A-IM
    - http/headers/Accept-Additions
    - http/headers/Accept-Datetime
    - http/headers/Accept-Encoding
    - http/headers/Accept-Features
    - http/headers/Accept-Patch
    - http/headers/Alternates
    - http/headers/Apply-To-Redirect-Ref
    - http/headers/Authentication-Info
    - http/headers/Close
    - http/headers/Connection
    - http/headers/Content-Base
    - http/headers/Content-Encoding
    - http/headers/Content-ID
    - http/headers/Content-Language
    - http/headers/Content-Script-Type
    - http/headers/Content-Style-Type
    - http/headers/Content-Version
    - http/headers/Cookie2
    - http/headers/DASL
    - http/headers/DAV
    - http/headers/Default-Style
    - http/headers/Delta-Base
    - http/headers/Depth
    - http/headers/Derived-From
    - http/headers/Destination
    - http/headers/Differential-ID
    - http/headers/Ext
    - http/headers/Forwarded
    - http/headers/Host
    - http/headers/IM
    - http/headers/If
    - http/headers/If-Schedule-Tag-Match
    - http/headers/Keep-Alive
    - http/headers/Label
    - http/headers/Location
    - http/headers/Lock-Token
    - http/headers/Man
    - http/headers/Max-Forwards
    - http/headers/Memento-Datetime
    - http/headers/Meter
    - http/headers/MIME-Version
    - http/headers/Negotiate
    - http/headers/Opt
    - http/headers/Ordering-Type
    - http/headers/Origin
    - http/headers/Overwrite
    - http/headers/P3P
    - http/headers/PEP
    - http/headers/PICS-Label
    - http/headers/Pep-Info
    - http/headers/Position
    - http/headers/Pragma
    - http/headers/Prefer
    - http/headers/Preference-Applied
    - http/headers/ProfileObject
    - http/headers/Proxy-Authentication-Info
    - http/headers/Proxy-Features
    - http/headers/Proxy-Instruction
    - http/headers/Public
    - http/headers/Redirect-Ref
    - http/headers/Retry-After
    - http/headers/Safe
    - http/headers/Schedule-Reply
    - http/headers/Schedule-Tag
    - http/headers/Sec-WebSocket-Accept
    - http/headers/Sec-WebSocket-Extensions
    - http/headers/Sec-WebSocket-Key
    - http/headers/Sec-WebSocket-Protocol
    - http/headers/Sec-WebSocket-Version
    - http/headers/Security-Scheme
    - http/headers/Set-Cookie
    - http/headers/Set-Cookie2
    - http/headers/Slug
    - http/headers/SoapAction
    - http/headers/Status-URI
    - http/headers/Strict-Transport-Security
    - http/headers/Surrogate-Capability
    - http/headers/Surrogate-Control
    - http/headers/TCN
    - http/headers/TE
    - http/headers/Timeout
    - http/headers/Trailer
    - http/headers/URI
    - http/headers/Upgrade
    - http/headers/Variant-Vary
    - http/headers/Vary
    - http/headers/Via
    - http/headers/Want-Digest
    - http/headers/Warning
    - http/headers/X-Frame-Options
uri: http/headers

---
The full list of HTTP headers is shared with MIME headers and is maintained by the IANA at [Message Headers](http://www.iana.org/assignments/message-headers/message-headers.xhtml)

## Headers by Function

### Informational

-   Main article: [Requesting resources](/w/index.php?title=http/requesting_resources&action=edit&redlink=1): GET, HEAD, OPTIONS
-   Main article: [Modification of resources](/w/index.php?title=http/modifying_resources&action=edit&redlink=1): PUT, PATCH
-   Main article: [Forms and scripts](/w/index.php?title=http/forms_and_scripts&action=edit&redlink=1): POST with HTML Forms, using 3xx Status codes
-   [User-Agent](/http/headers/User-Agent)
-   [Server](/http/headers/Server)
-   [From](/http/headers/From)
-   [Date](/http/headers/Date)
-   [Referer](/http/headers/Referer) [sic]

### Resource Metadata

-   Main article: [Resource metadata](/w/index.php?title=http/resource_metadata&action=edit&redlink=1): Link, Last-Modified, Content-Type, Allow, etc
-   [Content-Location](/http/headers/Content-Location)
-   [Link](/http/headers/Link)
-   [Last-Modified](/http/headers/Last-Modified)
-   [ETag](/http/headers/ETag)
-   [Content-MD5](/w/index.php?title=http/headers/Content-MD5&action=edit&redlink=1)
-   [Allow](/http/headers/Allow)

### Transfer Control

-   Main article: [Requesting resources](/w/index.php?title=http/requesting_resources&action=edit&redlink=1): GET, HEAD, OPTIONS
-   [Transfer-Encoding](/w/index.php?title=http/headers/Transfer-Encoding&action=edit&redlink=1)
-   [Content-Length](/w/index.php?title=http/headers/Content-Length&action=edit&redlink=1)
-   [Expect](/w/index.php?title=http/headers/Expect&action=edit&redlink=1): 100-continue

### Entity Body and Partial Content

-   Main article: [Partial content responses](/w/index.php?title=http/partial_responses&action=edit&redlink=1)
-   [Content-Range](/w/index.php?title=http/headers/Content-Range&action=edit&redlink=1)
-   [Accept-Ranges](/w/index.php?title=http/headers/Accept-Ranges&action=edit&redlink=1)
-   [If-Range](/http/headers/If-Range)
-   [Range](/http/headers/Range)

### Caching

-   Main article: [Layered requests](/w/index.php?title=http/layered_requests&action=edit&redlink=1) with proxies and gateways
-   [Expires](/http/headers/Expires)
-   [Date](/http/headers/Date)
-   [Age](/w/index.php?title=http/headers/Age&action=edit&redlink=1)
-   [Cache-Control](/http/headers/Cache-Control)
-   [ETag](/http/headers/ETag)
-   [Last-Modified](/http/headers/Last-Modified)
-   [Content-Location](/http/headers/Content-Location)

### Conditional Requests

-   Main article: [Caching](/w/index.php?title=http/caching&action=edit&redlink=1) and conditional requests
-   Main article: [Conditional updates](/w/index.php?title=http/conditional_updates&action=edit&redlink=1)
-   [If-Modified-Since](/http/headers/If-Modified-Since)
-   [If-Match](/http/headers/If-Match)
-   [If-Unmodified-Since](/http/headers/If-Unmodified-Since)
-   [If-None-Match](/http/headers/If-None-Match)
-   [If-Range](/http/headers/If-Range)
-   [ETag](/http/headers/ETag)
-   [Last-Modified](/http/headers/Last-Modified)

### Authentication and Access Control

-   Main article: [Access control](/w/index.php?title=http/access_control&action=edit&redlink=1)
-   [WWW-Authenticate](/w/index.php?title=http/headers/WWW-Authenticate&action=edit&redlink=1)
-   [Authorization](/http/headers/Authorization)
-   [Proxy-Authenticate](/w/index.php?title=http/headers/Proxy-Authenticate&action=edit&redlink=1)
-   [Proxy-Authorization](/w/index.php?title=http/headers/Proxy-Authorization&action=edit&redlink=1)

### Content-Type Negotiation

-   Main article: [Content negotiation](/w/index.php?title=http/content_negotiation&action=edit&redlink=1): Accept, Content-Location
-   [Accept](/http/headers/Accept)
-   [Accept-Charset](/w/index.php?title=http/headers/Accept-Charset&action=edit&redlink=1)
-   [Accept-Language](/w/index.php?title=http/headers/Accept-Language&action=edit&redlink=1)
-   [Accept-Ranges](/w/index.php?title=http/headers/Accept-Ranges&action=edit&redlink=1)

## Crafting New Headers

See [RFC7231 Section 8.3.1](http://tools.ietf.org/html/rfc7231#section-8.3.1).

If the response is identifying another resource, use the Link header with a URI as the relation name, e.g.:

    Link: <http://example.com/AcmeMetals>;rel="http://example.com/coin-minted-by"

## Table of Headers

|Header|Description|Reference|
|:-----|:----------|:--------|
|[A-IM](/w/index.php?title=http/headers/A-IM&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Accept](/http/headers/Accept)||[RFC7231, Section 5.3.2](http://tools.ietf.org/html/rfc7231#section-5.3.2)|
|[Accept-Additions](/w/index.php?title=http/headers/Accept-Additions&action=edit&redlink=1)|Used in Hyper Text Coffee Pot Control Protocol (HTCPCP/1.0)|[RFC2324](http://tools.ietf.org/html/rfc2324#section-2.2.2.1)|
|[Accept-Charset](/w/index.php?title=http/headers/Accept-Charset&action=edit&redlink=1)||[RFC7231, Section 5.3.3](http://tools.ietf.org/html/rfc7231#section-5.3.3)|
|[Accept-Datetime](/w/index.php?title=http/headers/Accept-Datetime&action=edit&redlink=1)||[RFC7089](http://tools.ietf.org/html/rfc7089)|
|[Accept-Encoding](/w/index.php?title=http/headers/Accept-Encoding&action=edit&redlink=1)||[RFC7231, Section 5.3.4](http://tools.ietf.org/html/rfc7231#section-5.3.4)|
|[Accept-Features](/w/index.php?title=http/headers/Accept-Features&action=edit&redlink=1)|Experimental|[RFC2995](http://tools.ietf.org/html/rfc2295#section-8.2)|
|[Accept-Language](/w/index.php?title=http/headers/Accept-Language&action=edit&redlink=1)|Locales that a user agent prefers|[RFC7231, Section 5.3.5](http://tools.ietf.org/html/rfc7231#section-5.3.5)|
|[Accept-Patch](/w/index.php?title=http/headers/Accept-Patch&action=edit&redlink=1)|Specifies media types that are acceptable for PATCH requests|[RFC5789](http://tools.ietf.org/html/rfc5789)|
|[Accept-Ranges](/w/index.php?title=http/headers/Accept-Ranges&action=edit&redlink=1)|Server indication of which range units it understands (e.g. byte)|[RFC7233, Section 2.3](http://tools.ietf.org/html/rfc7233#section-2.3)|
|[Age](/w/index.php?title=http/headers/Age&action=edit&redlink=1)|Estimate of how stale the resource is, in seconds, used by caches|[RFC7234, Section 5.1](http://tools.ietf.org/html/rfc7234#section-5.1)|
|[Allow](/http/headers/Allow)|Indicate which methods can be used on the resource|[RFC7231, Section 7.4.1](http://tools.ietf.org/html/rfc7231#section-7.4.1)|
|[Alternates](/w/index.php?title=http/headers/Alternates&action=edit&redlink=1)|Experimental|[RFC2295](http://tools.ietf.org/html/rfc2295)|
|[Apply-To-Redirect-Ref](/w/index.php?title=http/headers/Apply-To-Redirect-Ref&action=edit&redlink=1)||[RFC4437](http://tools.ietf.org/html/rfc4437)|
|[Authentication-Info](/w/index.php?title=http/headers/Authentication-Info&action=edit&redlink=1)|Control data and information about the authentication session|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Authorization](/http/headers/Authorization)|Credentials for accessing a resource on the server|[RFC7235, Section 4.2](http://tools.ietf.org/html/rfc7235#section-4.2)|
|[Cache-Control](/http/headers/Cache-Control)|Information for how and when to cache the resource|[RFC7234, Section 5.2](http://tools.ietf.org/html/rfc7234#section-5.2)|
|[Close](/w/index.php?title=http/headers/Close&action=edit&redlink=1)|Not actually a valid header. Reserved to prevent conflicts with [`Connection`](/w/index.php?title=http/headers/Connection&action=edit&redlink=1)`: close`|[RFC7230, Section 8.1](http://tools.ietf.org/html/rfc7230#section-8.1)|
|[Connection](/w/index.php?title=http/headers/Connection&action=edit&redlink=1)||[RFC7230, Section 6.1](http://tools.ietf.org/html/rfc7230#section-6.1)|
|[Content-Base](/w/index.php?title=http/headers/Content-Base&action=edit&redlink=1)|Provides a base URI for the document (largely unsupported and obsolete)|[RFC2068](http://tools.ietf.org/html/rfc2068)[RFC2616](http://www.iana.org/go/rfc2616)|
|[Content-Disposition](/http/headers/Content-Disposition)|Conveys additional information about how to process the response payload|[RFC6266](http://tools.ietf.org/html/rfc6266)|
|[Content-Encoding](/w/index.php?title=http/headers/Content-Encoding&action=edit&redlink=1)|See also [Transfer-Encoding](/w/index.php?title=http/headers/Transfer-Encoding&action=edit&redlink=1)|[RFC7231, Section 3.1.2.2](http://tools.ietf.org/html/rfc7231#section-3.1.2.2)|
|[Content-ID](/w/index.php?title=http/headers/Content-ID&action=edit&redlink=1)|Obsolete|[RFC4229](http://tools.ietf.org/html/rfc4229) [DRP](http://www.w3.org/TR/NOTE-drp-19970825)|
|[Content-Language](/w/index.php?title=http/headers/Content-Language&action=edit&redlink=1)|The locale/language of the entity-body|[RFC7231, Section 3.1.3.2](http://tools.ietf.org/html/rfc7231#section-3.1.3.2)|
|[Content-Length](/w/index.php?title=http/headers/Content-Length&action=edit&redlink=1)|The octet (byte) length of the attached entity-body|[RFC7230, Section 3.3.2](http://tools.ietf.org/html/rfc7230#section-3.3.2)|
|[Content-Location](/http/headers/Content-Location)|The URI of the attached entity-body|[RFC7231, Section 3.1.4.2](http://tools.ietf.org/html/rfc7231#section-3.1.4.2)|
|[Content-MD5](/w/index.php?title=http/headers/Content-MD5&action=edit&redlink=1)|Obsolete|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Content-Range](/w/index.php?title=http/headers/Content-Range&action=edit&redlink=1)|Identifies the enclose entity-body is a subset of the requested resource|[RFC7233, Section 4.2](http://tools.ietf.org/html/rfc7233#section-4.2)|
|[Content-Script-Type](/w/index.php?title=http/headers/Content-Script-Type&action=edit&redlink=1)||[HTML 4.01 Section 18.2.2](http://www.w3.org/TR/html401/interact/scripts.html#h-18.2.2)|
|[Content-Style-Type](/w/index.php?title=http/headers/Content-Style-Type&action=edit&redlink=1)||[HTML 4.01 Section 14.2.1](http://www.w3.org/TR/html401/present/styles.html#h-14.2.1)|
|[Content-Type](/http/headers/Content-Type)|The media type of the attached entity-body|[RFC7231, Section 3.1.1.5](http://tools.ietf.org/html/rfc7231#section-3.1.1.5)|
|[Content-Version](/w/index.php?title=http/headers/Content-Version&action=edit&redlink=1)|Obsolete|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Cookie](/http/headers/Cookie)|Declares a stored cookie value to the server|[RFC6265](http://tools.ietf.org/html/rfc6265)|
|[Cookie2](/w/index.php?title=http/headers/Cookie2&action=edit&redlink=1)|Declares a stored cookie value to the server; Obsolete|[RFC2965](http://tools.ietf.org/html/rfc2965)[RFC6265](http://www.iana.org/go/rfc6265)|
|[DASL](/w/index.php?title=http/headers/DASL&action=edit&redlink=1)||[RFC5323](http://tools.ietf.org/html/rfc5323)|
|[DAV](/w/index.php?title=http/headers/DAV&action=edit&redlink=1)|Used in WebDAV|[RFC4918](http://tools.ietf.org/html/rfc4918)|
|[Date](/http/headers/Date)|The date and time at which the message was originated|[RFC7231, Section 7.1.1.2](http://tools.ietf.org/html/rfc7231#section-7.1.1.2)|
|[Default-Style](/w/index.php?title=http/headers/Default-Style&action=edit&redlink=1)||[HTML 4.01 Section 14.3.2](http://www.w3.org/TR/html401/present/styles.html#h-14.3.2)|
|[Delta-Base](/w/index.php?title=http/headers/Delta-Base&action=edit&redlink=1)|The entity tag of the base instance against which the delta applies|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Depth](/w/index.php?title=http/headers/Depth&action=edit&redlink=1)|Used in WebDAV|[RFC4918](http://tools.ietf.org/html/rfc4918)|
|[Derived-From](/w/index.php?title=http/headers/Derived-From&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Destination](/w/index.php?title=http/headers/Destination&action=edit&redlink=1)|Used in WebDAV|[RFC4918](http://tools.ietf.org/html/rfc4918)|
|[Differential-ID](/w/index.php?title=http/headers/Differential-ID&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Digest](/http/headers/Digest)|Indicates a hash/digest for the full resource|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[ETag](/http/headers/ETag)|Differentiates between multiple versions/representations of the same resource|[RFC7232, Section 2.3](http://tools.ietf.org/html/rfc7232#section-2.3)|
|[Expect](/w/index.php?title=http/headers/Expect&action=edit&redlink=1)|Require that downstream nodes support specified functionality|[RFC7231, Section 5.1.1](http://tools.ietf.org/html/rfc7231#section-5.1.1)|
|[Expires](/http/headers/Expires)|Controls caching|[RFC7234, Section 5.3](http://tools.ietf.org/html/rfc7234#section-5.3)|
|[Ext](/w/index.php?title=http/headers/Ext&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Forwarded](/w/index.php?title=http/headers/Forwarded&action=edit&redlink=1)|Shows where the message originated from, further upstream|[RFC7239](http://tools.ietf.org/html/rfc7239)|
|[From](/http/headers/From)|Contact information for the user making the request, especially for Web spiders|[RFC7231, Section 5.5.1](http://tools.ietf.org/html/rfc7231#section-5.5.1)|
|[Host](/w/index.php?title=http/headers/Host&action=edit&redlink=1)|Hostname component of the request-URI (Required)|[RFC7230, Section 5.4](http://tools.ietf.org/html/rfc7230#section-5.4)|
|[IM](/w/index.php?title=http/headers/IM&action=edit&redlink=1)|Instance Manipulation|[RFC4229](http://tools.ietf.org/html/rfc4229) [RFC 3229](http://tools.ietf.org/html/rfc3229#section-10.5.2)|
|[If](/w/index.php?title=http/headers/If&action=edit&redlink=1)|Used in WebDAV|[RFC4918](http://tools.ietf.org/html/rfc4918)|
|[If-Match](/http/headers/If-Match)|Conditional request header|[RFC7232, Section 3.1](http://tools.ietf.org/html/rfc7232#section-3.1)|
|[If-Modified-Since](/http/headers/If-Modified-Since)|Conditional request header|[RFC7232, Section 3.3](http://tools.ietf.org/html/rfc7232#section-3.3)|
|[If-None-Match](/http/headers/If-None-Match)|Conditional request header|[RFC7232, Section 3.2](http://tools.ietf.org/html/rfc7232#section-3.2)|
|[If-Range](/http/headers/If-Range)|Conditional request header|[RFC7233, Section 3.2](http://tools.ietf.org/html/rfc7233#section-3.2)|
|[If-Schedule-Tag-Match](/w/index.php?title=http/headers/If-Schedule-Tag-Match&action=edit&redlink=1)|Part of Scheduling Extensions to CalDAV|[RFC6638](http://tools.ietf.org/html/rfc6638)|
|[If-Unmodified-Since](/http/headers/If-Unmodified-Since)|Conditional request header|[RFC7232, Section 3.4](http://tools.ietf.org/html/rfc7232#section-3.4)|
|[Keep-Alive](/w/index.php?title=http/headers/Keep-Alive&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Label](/w/index.php?title=http/headers/Label&action=edit&redlink=1)|Used in WebDAV|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Last-Modified](/http/headers/Last-Modified)||[RFC7232, Section 2.2](http://tools.ietf.org/html/rfc7232#section-2.2)|
|[Link](/http/headers/Link)|Declares a link relationship to another resource|[RFC5988](http://tools.ietf.org/html/rfc5988)|
|[Location](/w/index.php?title=http/headers/Location&action=edit&redlink=1)|Points to another resource, typically for redirection purposes|[RFC7231, Section 7.1.2](http://tools.ietf.org/html/rfc7231#section-7.1.2)|
|[Lock-Token](/w/index.php?title=http/headers/Lock-Token&action=edit&redlink=1)|Used in WebDAV|[RFC4918](http://tools.ietf.org/html/rfc4918)|
|[Man](/w/index.php?title=http/headers/Man&action=edit&redlink=1)|Experimental|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Max-Forwards](/w/index.php?title=http/headers/Max-Forwards&action=edit&redlink=1)|Limit the number of forwards, similar to a TTL|[RFC7231, Section 5.1.2](http://tools.ietf.org/html/rfc7231#section-5.1.2)|
|[Memento-Datetime](/w/index.php?title=http/headers/Memento-Datetime&action=edit&redlink=1)||[RFC7089](http://tools.ietf.org/html/rfc7089)|
|[Meter](/w/index.php?title=http/headers/Meter&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229) [RFC2227](http://tools.ietf.org/html/rfc2227)|
|[MIME-Version](/w/index.php?title=http/headers/MIME-Version&action=edit&redlink=1)|The HTTP Message is also MIME compatible (obsolete)|[RFC7231, Appendix A.1](http://tools.ietf.org/html/rfc7231#appendix-A.1)|
|[Negotiate](/w/index.php?title=http/headers/Negotiate&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229) [RFC2295](http://tools.ietf.org/html/rfc2295)|
|[Opt](/w/index.php?title=http/headers/Opt&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Ordering-Type](/w/index.php?title=http/headers/Ordering-Type&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Origin](/w/index.php?title=http/headers/Origin&action=edit&redlink=1)||[RFC6454](http://tools.ietf.org/html/rfc6454)|
|[Overwrite](/w/index.php?title=http/headers/Overwrite&action=edit&redlink=1)|Used in WebDAV|[RFC4918](http://tools.ietf.org/html/rfc4918)|
|[P3P](/w/index.php?title=http/headers/P3P&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[PEP](/w/index.php?title=http/headers/PEP&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[PICS-Label](/w/index.php?title=http/headers/PICS-Label&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Pep-Info](/w/index.php?title=http/headers/Pep-Info&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Position](/w/index.php?title=http/headers/Position&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Pragma](/w/index.php?title=http/headers/Pragma&action=edit&redlink=1)|(Deprecated HTTP/1.0 header)|[RFC7234, Section 5.4](http://tools.ietf.org/html/rfc7234#section-5.4)|
|[Prefer](/w/index.php?title=http/headers/Prefer&action=edit&redlink=1)|Indicate a preference for how the server should respond to a query|[RFC7240](http://tools.ietf.org/html/rfc7240)|
|[Preference-Applied](/w/index.php?title=http/headers/Preference-Applied&action=edit&redlink=1)||[RFC7240](http://tools.ietf.org/html/rfc7240)|
|[ProfileObject](/w/index.php?title=http/headers/ProfileObject&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Proxy-Authenticate](/w/index.php?title=http/headers/Proxy-Authenticate&action=edit&redlink=1)|Use of proxy requires authentication|[RFC7235, Section 4.3](http://tools.ietf.org/html/rfc7235#section-4.3)|
|[Proxy-Authentication-Info](/w/index.php?title=http/headers/Proxy-Authentication-Info&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Proxy-Authorization](/w/index.php?title=http/headers/Proxy-Authorization&action=edit&redlink=1)|Send credentials to a proxy|[RFC7235, Section 4.4](http://tools.ietf.org/html/rfc7235#section-4.4)|
|[Proxy-Features](/w/index.php?title=http/headers/Proxy-Features&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Proxy-Instruction](/w/index.php?title=http/headers/Proxy-Instruction&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Public](/w/index.php?title=http/headers/Public&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Range](/http/headers/Range)|Request a subset of the resource|[RFC7233, Section 3.1](http://tools.ietf.org/html/rfc7233#section-3.1)|
|[Redirect-Ref](/w/index.php?title=http/headers/Redirect-Ref&action=edit&redlink=1)||[RFC4437](http://tools.ietf.org/html/rfc4437)|
|[Referer](/http/headers/Referer)|(Sic) Page that was linked from|[RFC7231, Section 5.5.2](http://tools.ietf.org/html/rfc7231#section-5.5.2)|
|[Retry-After](/w/index.php?title=http/headers/Retry-After&action=edit&redlink=1)||[RFC7231, Section 7.1.3](http://tools.ietf.org/html/rfc7231#section-7.1.3)|
|[Safe](/w/index.php?title=http/headers/Safe&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Schedule-Reply](/w/index.php?title=http/headers/Schedule-Reply&action=edit&redlink=1)|Part of Scheduling Extensions to CalDAV|[RFC6638](http://tools.ietf.org/html/rfc6638)|
|[Schedule-Tag](/w/index.php?title=http/headers/Schedule-Tag&action=edit&redlink=1)|Part of Scheduling Extensions to CalDAV|[RFC6638](http://tools.ietf.org/html/rfc6638)|
|[Sec-WebSocket-Accept](/w/index.php?title=http/headers/Sec-WebSocket-Accept&action=edit&redlink=1)|Used for negotiating a WebSocket connection|[RFC6455](http://tools.ietf.org/html/rfc6455)|
|[Sec-WebSocket-Extensions](/w/index.php?title=http/headers/Sec-WebSocket-Extensions&action=edit&redlink=1)|Used for negotiating a WebSocket connection|[RFC6455](http://tools.ietf.org/html/rfc6455)|
|[Sec-WebSocket-Key](/w/index.php?title=http/headers/Sec-WebSocket-Key&action=edit&redlink=1)|Used for negotiating a WebSocket connection|[RFC6455](http://tools.ietf.org/html/rfc6455)|
|[Sec-WebSocket-Protocol](/w/index.php?title=http/headers/Sec-WebSocket-Protocol&action=edit&redlink=1)|Used for negotiating a WebSocket connection|[RFC6455](http://tools.ietf.org/html/rfc6455)|
|[Sec-WebSocket-Version](/w/index.php?title=http/headers/Sec-WebSocket-Version&action=edit&redlink=1)|Used for negotiating a WebSocket connection|[RFC6455](http://tools.ietf.org/html/rfc6455)|
|[Security-Scheme](/w/index.php?title=http/headers/Security-Scheme&action=edit&redlink=1)|Used to indicate S-HTTP support (not to be confused with HTTPS)|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Server](/http/headers/Server)|Indicates the server's software and version|[RFC7231, Section 7.4.2](http://tools.ietf.org/html/rfc7231#section-7.4.2)|
|[Set-Cookie](/w/index.php?title=http/headers/Set-Cookie&action=edit&redlink=1)|Request to store a cookie on the user-agent|[RFC6265](http://tools.ietf.org/html/rfc6265)|
|[Set-Cookie2](/w/index.php?title=http/headers/Set-Cookie2&action=edit&redlink=1)|Request to store a cookie on the user-agent; Obsolete|[RFC2965](http://tools.ietf.org/html/rfc2965)[RFC6265](http://www.iana.org/go/rfc6265)|
|[Slug](/w/index.php?title=http/headers/Slug&action=edit&redlink=1)|Specifies a "slug" string to be used in the generation of URLs of new resources. Used by the Atom Publishing Protocol.|[RFC5023](http://tools.ietf.org/html/rfc5023)|
|[SoapAction](/w/index.php?title=http/headers/SoapAction&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Status-URI](/w/index.php?title=http/headers/Status-URI&action=edit&redlink=1)|Used by WebDAV|[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Strict-Transport-Security](/w/index.php?title=http/headers/Strict-Transport-Security&action=edit&redlink=1)|HSTS, asks that future requests must only go over TLS|[RFC6797](http://tools.ietf.org/html/rfc6797)|
|[Surrogate-Capability](/w/index.php?title=http/headers/Surrogate-Capability&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Surrogate-Control](/w/index.php?title=http/headers/Surrogate-Control&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[TCN](/w/index.php?title=http/headers/TCN&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[TE](/w/index.php?title=http/headers/TE&action=edit&redlink=1)||[RFC7230, Section 4.3](http://tools.ietf.org/html/rfc7230#section-4.3)|
|[Timeout](/w/index.php?title=http/headers/Timeout&action=edit&redlink=1)|Used in WebDAV|[RFC4918](http://tools.ietf.org/html/rfc4918)|
|[Trailer](/w/index.php?title=http/headers/Trailer&action=edit&redlink=1)||[RFC7230, Section 4.4](http://tools.ietf.org/html/rfc7230#section-4.4)|
|[Transfer-Encoding](/w/index.php?title=http/headers/Transfer-Encoding&action=edit&redlink=1)|Specifies how the payload has been compressed. See also [Content-Encoding](/w/index.php?title=http/headers/Content-Encoding&action=edit&redlink=1)|[RFC7230, Section 3.3.1](http://tools.ietf.org/html/rfc7230#section-3.3.1)|
|[URI](/w/index.php?title=http/headers/URI&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Upgrade](/w/index.php?title=http/headers/Upgrade&action=edit&redlink=1)||[RFC7230, Section 6.7](http://tools.ietf.org/html/rfc7230#section-6.7)|
|[User-Agent](/http/headers/User-Agent)|Indicates the user agent's software and version|[RFC7231, Section 5.5.3](http://tools.ietf.org/html/rfc7231#section-5.5.3)|
|[Variant-Vary](/w/index.php?title=http/headers/Variant-Vary&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Vary](/w/index.php?title=http/headers/Vary&action=edit&redlink=1)|The server's response was chosen based on the specified headers|[RFC7231, Section 7.1.4](http://tools.ietf.org/html/rfc7231#section-7.1.4)|
|[Via](/w/index.php?title=http/headers/Via&action=edit&redlink=1)||[RFC7230, Section 5.7.1](http://tools.ietf.org/html/rfc7230#section-5.7.1)|
|[WWW-Authenticate](/w/index.php?title=http/headers/WWW-Authenticate&action=edit&redlink=1)||[RFC7235, Section 4.1](http://tools.ietf.org/html/rfc7235#section-4.1)|
|[Want-Digest](/w/index.php?title=http/headers/Want-Digest&action=edit&redlink=1)||[RFC4229](http://tools.ietf.org/html/rfc4229)|
|[Warning](/w/index.php?title=http/headers/Warning&action=edit&redlink=1)||[RFC7234, Section 5.5](http://tools.ietf.org/html/rfc7234#section-5.5)|
|[X-Frame-Options](/w/index.php?title=http/headers/X-Frame-Options&action=edit&redlink=1)|Older variation on Frame-Options header|[RFC7034](http://tools.ietf.org/html/rfc7034) [CSP](http://www.w3.org/TR/CSP11/)|

