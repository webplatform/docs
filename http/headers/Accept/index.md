---
title: Accept
tags:
  - HTTP
  - Headers
summary: 'Used by user agents to specify response media types that are acceptable.'
uri: http/headers/Accept

---
# Accept

## Summary

Used by user agents to specify response media types that are acceptable.

## Overview table

Direction
:   Request
Features
:

## Syntax

    Accept = #( media-range [ accept-params ] )
    media-range    = ( "*/*"
                     / ( type "/" "*" )
                     / ( type "/" subtype )
                     ) *( OWS ";" OWS parameter )
    accept-params  = weight *( accept-ext )
    accept-ext = OWS ";" OWS token [ "=" ( token / quoted-string ) ]

## Examples

Prefer HTML or text/x-c, or text/x-dvi if it's the best the server has after a 20% markdown in quality, or plain text after a 50% markdown in quality:

``` {.other}
Accept: text/plain; q=0.5, text/html, text/x-dvi; q=0.8, text/x-c
```

Prefer XHTML or HTML, or generic XML with a reduced preference, or else any content:

``` {.other}
Accept: text/html, application/xhtml+xml, application/xml;q=0.9, */*;q=0.8
```

## Related specifications

Specification
:   Status
[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-5.3.2)
:

