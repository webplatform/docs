---
title: 'If-Modified-Since'
compatibility:
  feature: If-Modified-Since
  topic: http
overview_table:
  Direction: Request
  Features: ''
summary: 'Makes the request conditional on the server''s resource having been updated recently, for refreshing caches.'
tags:
  - HTTP_Headers
uri: http/headers/If-Modified-Since

---
## Summary

Makes the request conditional on the server's resource having been updated recently, for refreshing caches.

## Overview table

Direction
:   Request

Features
:

## Syntax

    If-Modified-Since = HTTP-date

## Examples

``` html
If-Modified-Since: Sat, 29 Oct 1994 19:43:31 GMT
```

## Related specifications

[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.3)
:

