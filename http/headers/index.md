---
title: headers
uri: http/headers
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

Header
:   Description
[A-IM](/w/index.php?title=http/headers/A-IM&action=edit&redlink=1)
:
[Accept](/http/headers/Accept)
:
[Accept-Additions](/w/index.php?title=http/headers/Accept-Additions&action=edit&redlink=1)
:   Used in Hyper Text Coffee Pot Control Protocol (HTCPCP/1.0)
[Accept-Charset](/w/index.php?title=http/headers/Accept-Charset&action=edit&redlink=1)
:
[Accept-Datetime](/w/index.php?title=http/headers/Accept-Datetime&action=edit&redlink=1)
:
[Accept-Encoding](/w/index.php?title=http/headers/Accept-Encoding&action=edit&redlink=1)
:
[Accept-Features](/w/index.php?title=http/headers/Accept-Features&action=edit&redlink=1)
:   Experimental
[Accept-Language](/w/index.php?title=http/headers/Accept-Language&action=edit&redlink=1)
:   Locales that a user agent prefers
[Accept-Patch](/w/index.php?title=http/headers/Accept-Patch&action=edit&redlink=1)
:   Specifies media types that are acceptable for PATCH requests
[Accept-Ranges](/w/index.php?title=http/headers/Accept-Ranges&action=edit&redlink=1)
:   Server indication of which range units it understands (e.g. byte)
[Age](/w/index.php?title=http/headers/Age&action=edit&redlink=1)
:   Estimate of how stale the resource is, in seconds, used by caches
[Allow](/http/headers/Allow)
:   Indicate which methods can be used on the resource
[Alternates](/w/index.php?title=http/headers/Alternates&action=edit&redlink=1)
:   Experimental
[Apply-To-Redirect-Ref](/w/index.php?title=http/headers/Apply-To-Redirect-Ref&action=edit&redlink=1)
:
[Authentication-Info](/w/index.php?title=http/headers/Authentication-Info&action=edit&redlink=1)
:   Control data and information about the authentication session
[Authorization](/http/headers/Authorization)
:   Credentials for accessing a resource on the server
[Cache-Control](/http/headers/Cache-Control)
:   Information for how and when to cache the resource
[Close](/w/index.php?title=http/headers/Close&action=edit&redlink=1)
:   Not actually a valid header. Reserved to prevent conflicts with [`Connection`](/w/index.php?title=http/headers/Connection&action=edit&redlink=1)`: close`
[Connection](/w/index.php?title=http/headers/Connection&action=edit&redlink=1)
:
[Content-Base](/w/index.php?title=http/headers/Content-Base&action=edit&redlink=1)
:   Provides a base URI for the document (largely unsupported and obsolete)
[Content-Disposition](/http/headers/Content-Disposition)
:   Conveys additional information about how to process the response payload
[Content-Encoding](/w/index.php?title=http/headers/Content-Encoding&action=edit&redlink=1)
:   See also [Transfer-Encoding](/w/index.php?title=http/headers/Transfer-Encoding&action=edit&redlink=1)
[Content-ID](/w/index.php?title=http/headers/Content-ID&action=edit&redlink=1)
:   Obsolete
[Content-Language](/w/index.php?title=http/headers/Content-Language&action=edit&redlink=1)
:   The locale/language of the entity-body
[Content-Length](/w/index.php?title=http/headers/Content-Length&action=edit&redlink=1)
:   The octet (byte) length of the attached entity-body
[Content-Location](/http/headers/Content-Location)
:   The URI of the attached entity-body
[Content-MD5](/w/index.php?title=http/headers/Content-MD5&action=edit&redlink=1)
:   Obsolete
[Content-Range](/w/index.php?title=http/headers/Content-Range&action=edit&redlink=1)
:   Identifies the enclose entity-body is a subset of the requested resource
[Content-Script-Type](/w/index.php?title=http/headers/Content-Script-Type&action=edit&redlink=1)
:
[Content-Style-Type](/w/index.php?title=http/headers/Content-Style-Type&action=edit&redlink=1)
:
[Content-Type](/http/headers/Content-Type)
:   The media type of the attached entity-body
[Content-Version](/w/index.php?title=http/headers/Content-Version&action=edit&redlink=1)
:   Obsolete
[Cookie](/http/headers/Cookie)
:   Declares a stored cookie value to the server
[Cookie2](/w/index.php?title=http/headers/Cookie2&action=edit&redlink=1)
:   Declares a stored cookie value to the server; Obsolete
[DASL](/w/index.php?title=http/headers/DASL&action=edit&redlink=1)
:
[DAV](/w/index.php?title=http/headers/DAV&action=edit&redlink=1)
:   Used in WebDAV
[Date](/http/headers/Date)
:   The date and time at which the message was originated
[Default-Style](/w/index.php?title=http/headers/Default-Style&action=edit&redlink=1)
:
[Delta-Base](/w/index.php?title=http/headers/Delta-Base&action=edit&redlink=1)
:   The entity tag of the base instance against which the delta applies
[Depth](/w/index.php?title=http/headers/Depth&action=edit&redlink=1)
:   Used in WebDAV
[Derived-From](/w/index.php?title=http/headers/Derived-From&action=edit&redlink=1)
:
[Destination](/w/index.php?title=http/headers/Destination&action=edit&redlink=1)
:   Used in WebDAV
[Differential-ID](/w/index.php?title=http/headers/Differential-ID&action=edit&redlink=1)
:
[Digest](/http/headers/Digest)
:   Indicates a hash/digest for the full resource
[ETag](/http/headers/ETag)
:   Differentiates between multiple versions/representations of the same resource
[Expect](/w/index.php?title=http/headers/Expect&action=edit&redlink=1)
:   Require that downstream nodes support specified functionality
[Expires](/http/headers/Expires)
:   Controls caching
[Ext](/w/index.php?title=http/headers/Ext&action=edit&redlink=1)
:
[Forwarded](/w/index.php?title=http/headers/Forwarded&action=edit&redlink=1)
:   Shows where the message originated from, further upstream
[From](/http/headers/From)
:   Contact information for the user making the request, especially for Web spiders
[Host](/w/index.php?title=http/headers/Host&action=edit&redlink=1)
:   Hostname component of the request-URI (Required)
[IM](/w/index.php?title=http/headers/IM&action=edit&redlink=1)
:   Instance Manipulation
[If](/w/index.php?title=http/headers/If&action=edit&redlink=1)
:   Used in WebDAV
[If-Match](/http/headers/If-Match)
:   Conditional request header
[If-Modified-Since](/http/headers/If-Modified-Since)
:   Conditional request header
[If-None-Match](/http/headers/If-None-Match)
:   Conditional request header
[If-Range](/http/headers/If-Range)
:   Conditional request header
[If-Schedule-Tag-Match](/w/index.php?title=http/headers/If-Schedule-Tag-Match&action=edit&redlink=1)
:   Part of Scheduling Extensions to CalDAV
[If-Unmodified-Since](/http/headers/If-Unmodified-Since)
:   Conditional request header
[Keep-Alive](/w/index.php?title=http/headers/Keep-Alive&action=edit&redlink=1)
:
[Label](/w/index.php?title=http/headers/Label&action=edit&redlink=1)
:   Used in WebDAV
[Last-Modified](/http/headers/Last-Modified)
:
[Link](/http/headers/Link)
:   Declares a link relationship to another resource
[Location](/w/index.php?title=http/headers/Location&action=edit&redlink=1)
:   Points to another resource, typically for redirection purposes
[Lock-Token](/w/index.php?title=http/headers/Lock-Token&action=edit&redlink=1)
:   Used in WebDAV
[Man](/w/index.php?title=http/headers/Man&action=edit&redlink=1)
:   Experimental
[Max-Forwards](/w/index.php?title=http/headers/Max-Forwards&action=edit&redlink=1)
:   Limit the number of forwards, similar to a TTL
[Memento-Datetime](/w/index.php?title=http/headers/Memento-Datetime&action=edit&redlink=1)
:
[Meter](/w/index.php?title=http/headers/Meter&action=edit&redlink=1)
:
[MIME-Version](/w/index.php?title=http/headers/MIME-Version&action=edit&redlink=1)
:   The HTTP Message is also MIME compatible (obsolete)
[Negotiate](/w/index.php?title=http/headers/Negotiate&action=edit&redlink=1)
:
[Opt](/w/index.php?title=http/headers/Opt&action=edit&redlink=1)
:
[Ordering-Type](/w/index.php?title=http/headers/Ordering-Type&action=edit&redlink=1)
:
[Origin](/w/index.php?title=http/headers/Origin&action=edit&redlink=1)
:
[Overwrite](/w/index.php?title=http/headers/Overwrite&action=edit&redlink=1)
:   Used in WebDAV
[P3P](/w/index.php?title=http/headers/P3P&action=edit&redlink=1)
:
[PEP](/w/index.php?title=http/headers/PEP&action=edit&redlink=1)
:
[PICS-Label](/w/index.php?title=http/headers/PICS-Label&action=edit&redlink=1)
:
[Pep-Info](/w/index.php?title=http/headers/Pep-Info&action=edit&redlink=1)
:
[Position](/w/index.php?title=http/headers/Position&action=edit&redlink=1)
:
[Pragma](/w/index.php?title=http/headers/Pragma&action=edit&redlink=1)
:   (Deprecated HTTP/1.0 header)
[Prefer](/w/index.php?title=http/headers/Prefer&action=edit&redlink=1)
:   Indicate a preference for how the server should respond to a query
[Preference-Applied](/w/index.php?title=http/headers/Preference-Applied&action=edit&redlink=1)
:
[ProfileObject](/w/index.php?title=http/headers/ProfileObject&action=edit&redlink=1)
:
[Proxy-Authenticate](/w/index.php?title=http/headers/Proxy-Authenticate&action=edit&redlink=1)
:   Use of proxy requires authentication
[Proxy-Authentication-Info](/w/index.php?title=http/headers/Proxy-Authentication-Info&action=edit&redlink=1)
:
[Proxy-Authorization](/w/index.php?title=http/headers/Proxy-Authorization&action=edit&redlink=1)
:   Send credentials to a proxy
[Proxy-Features](/w/index.php?title=http/headers/Proxy-Features&action=edit&redlink=1)
:
[Proxy-Instruction](/w/index.php?title=http/headers/Proxy-Instruction&action=edit&redlink=1)
:
[Public](/w/index.php?title=http/headers/Public&action=edit&redlink=1)
:
[Range](/http/headers/Range)
:   Request a subset of the resource
[Redirect-Ref](/w/index.php?title=http/headers/Redirect-Ref&action=edit&redlink=1)
:
[Referer](/http/headers/Referer)
:   (Sic) Page that was linked from
[Retry-After](/w/index.php?title=http/headers/Retry-After&action=edit&redlink=1)
:
[Safe](/w/index.php?title=http/headers/Safe&action=edit&redlink=1)
:
[Schedule-Reply](/w/index.php?title=http/headers/Schedule-Reply&action=edit&redlink=1)
:   Part of Scheduling Extensions to CalDAV
[Schedule-Tag](/w/index.php?title=http/headers/Schedule-Tag&action=edit&redlink=1)
:   Part of Scheduling Extensions to CalDAV
[Sec-WebSocket-Accept](/w/index.php?title=http/headers/Sec-WebSocket-Accept&action=edit&redlink=1)
:   Used for negotiating a WebSocket connection
[Sec-WebSocket-Extensions](/w/index.php?title=http/headers/Sec-WebSocket-Extensions&action=edit&redlink=1)
:   Used for negotiating a WebSocket connection
[Sec-WebSocket-Key](/w/index.php?title=http/headers/Sec-WebSocket-Key&action=edit&redlink=1)
:   Used for negotiating a WebSocket connection
[Sec-WebSocket-Protocol](/w/index.php?title=http/headers/Sec-WebSocket-Protocol&action=edit&redlink=1)
:   Used for negotiating a WebSocket connection
[Sec-WebSocket-Version](/w/index.php?title=http/headers/Sec-WebSocket-Version&action=edit&redlink=1)
:   Used for negotiating a WebSocket connection
[Security-Scheme](/w/index.php?title=http/headers/Security-Scheme&action=edit&redlink=1)
:   Used to indicate S-HTTP support (not to be confused with HTTPS)
[Server](/http/headers/Server)
:   Indicates the server's software and version
[Set-Cookie](/w/index.php?title=http/headers/Set-Cookie&action=edit&redlink=1)
:   Request to store a cookie on the user-agent
[Set-Cookie2](/w/index.php?title=http/headers/Set-Cookie2&action=edit&redlink=1)
:   Request to store a cookie on the user-agent; Obsolete
[Slug](/w/index.php?title=http/headers/Slug&action=edit&redlink=1)
:   Specifies a "slug" string to be used in the generation of URLs of new resources. Used by the Atom Publishing Protocol.
[SoapAction](/w/index.php?title=http/headers/SoapAction&action=edit&redlink=1)
:
[Status-URI](/w/index.php?title=http/headers/Status-URI&action=edit&redlink=1)
:   Used by WebDAV
[Strict-Transport-Security](/w/index.php?title=http/headers/Strict-Transport-Security&action=edit&redlink=1)
:   HSTS, asks that future requests must only go over TLS
[Surrogate-Capability](/w/index.php?title=http/headers/Surrogate-Capability&action=edit&redlink=1)
:
[Surrogate-Control](/w/index.php?title=http/headers/Surrogate-Control&action=edit&redlink=1)
:
[TCN](/w/index.php?title=http/headers/TCN&action=edit&redlink=1)
:
[TE](/w/index.php?title=http/headers/TE&action=edit&redlink=1)
:
[Timeout](/w/index.php?title=http/headers/Timeout&action=edit&redlink=1)
:   Used in WebDAV
[Trailer](/w/index.php?title=http/headers/Trailer&action=edit&redlink=1)
:
[Transfer-Encoding](/w/index.php?title=http/headers/Transfer-Encoding&action=edit&redlink=1)
:   Specifies how the payload has been compressed. See also [Content-Encoding](/w/index.php?title=http/headers/Content-Encoding&action=edit&redlink=1)
[URI](/w/index.php?title=http/headers/URI&action=edit&redlink=1)
:
[Upgrade](/w/index.php?title=http/headers/Upgrade&action=edit&redlink=1)
:
[User-Agent](/http/headers/User-Agent)
:   Indicates the user agent's software and version
[Variant-Vary](/w/index.php?title=http/headers/Variant-Vary&action=edit&redlink=1)
:
[Vary](/w/index.php?title=http/headers/Vary&action=edit&redlink=1)
:   The server's response was chosen based on the specified headers
[Via](/w/index.php?title=http/headers/Via&action=edit&redlink=1)
:
[WWW-Authenticate](/w/index.php?title=http/headers/WWW-Authenticate&action=edit&redlink=1)
:
[Want-Digest](/w/index.php?title=http/headers/Want-Digest&action=edit&redlink=1)
:
[Warning](/w/index.php?title=http/headers/Warning&action=edit&redlink=1)
:
[X-Frame-Options](/w/index.php?title=http/headers/X-Frame-Options&action=edit&redlink=1)
:   Older variation on Frame-Options header
