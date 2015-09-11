---
title: Server
overview_table:
  Direction: Response
  Features: ''
summary: 'Contains information about the software used by the origin server to handle the request.'
tags:
  - HTTP
  - Headers
uri: http/headers/Server

---
## <span>Summary</span>

Contains information about the software used by the origin server to handle the request.

## <span>Overview table</span>

Direction
:   Response

Features
:

## <span>Syntax</span>

    Server = product *( RWS ( product / comment ) )
    product = token ["/" product-version]
    product-version = token

## <span>Examples</span>

```
User-Agent: CERN-LineMode/2.15 libwww/2.17b3
```

``` html
Server: Apache/2.2.22 (Debian)
```

## <span>Related specifications</span>

[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-7.4.2)
:

