---
title: If-Unmodified-Since
overview_table:
  Direction: Request
  Features: ''
summary: 'Makes a request conditional on having a certain last-modified timestamp, used to prevent &quot;lost updates&quot; when modifying resources.'
tags:
  - HTTP
  - Headers
uri: http/headers/If-Unmodified-Since

---
## <span>Summary</span>

Makes a request conditional on having a certain last-modified timestamp, used to prevent &quot;lost updates&quot; when modifying resources.

## <span>Overview table</span>

Direction
:   Request

Features
:

## <span>Syntax</span>

    If-Unmodified-Since = HTTP-date

## <span>Examples</span>

``` html
If-Unmodified-Since: Sat, 29 Oct 1994 19:43:31 GMT
```

## <span>Related specifications</span>

[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.4)
:

