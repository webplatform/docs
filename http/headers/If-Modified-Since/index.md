---
title: If-Modified-Since
overview_table:
  Direction: Request
  Features: ''
summary: 'Makes the request conditional on the server''s resource having been updated recently, for refreshing caches.'
tags:
  - HTTP
  - Headers
uri: http/headers/If-Modified-Since

---
## <span>Summary</span>

Makes the request conditional on the server's resource having been updated recently, for refreshing caches.

## <span>Overview table</span>

Direction
:   Request

Features
:

## <span>Syntax</span>

    If-Modified-Since = HTTP-date

## <span>Examples</span>

``` html
If-Modified-Since: Sat, 29 Oct 1994 19:43:31 GMT
```

## <span>Related specifications</span>

[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.3)
:

