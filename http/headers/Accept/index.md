---
title: Accept
overview_table:
  Direction: Request
  Features: ''
summary: 'Used by user agents to specify response media types that are acceptable.'
tags:
  - HTTP
  - Headers
uri: http/headers/Accept

---
## <span>Summary</span>

Used by user agents to specify response media types that are acceptable.

## <span>Overview table</span>

Direction
:   Request

Features
:

## <span>Syntax</span>

    Accept = #( media-range [ accept-params ] )
    media-range    = ( "*/*"
                     / ( type "/" "*" )
                     / ( type "/" subtype )
                     ) *( OWS ";" OWS parameter )
    accept-params  = weight *( accept-ext )
    accept-ext = OWS ";" OWS token [ "=" ( token / quoted-string ) ]

## <span>Examples</span>

Prefer HTML or text/x-c, or text/x-dvi if it's the best the server has after a 20% markdown in quality, or plain text after a 50% markdown in quality:

```
Accept: text/plain; q=0.5, text/html, text/x-dvi; q=0.8, text/x-c
```

Prefer XHTML or HTML, or generic XML with a reduced preference, or else any content:

```
Accept: text/html, application/xhtml+xml, application/xml;q=0.9, */*;q=0.8
```

## <span>Related specifications</span>

[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-5.3.2)
:

