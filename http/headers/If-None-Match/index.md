---
title: If-None-Match
overview_table:
  Direction: Request
  Features: ''
summary: 'Makes a request conditional on a resource having changed from the specified ETag (version or representation), for refreshing caches.'
tags:
  - HTTP
  - Headers
uri: http/headers/If-None-Match

---
## Summary

Makes a request conditional on a resource having changed from the specified ETag (version or representation), for refreshing caches.

## Overview table

Direction
:   Request

Features
:

## Syntax

    If-None-Match = "*" / 1#entity-tag

## Examples

``` html
If-None-Match: "xyzzy"
```

``` html
If-None-Match: W/"xyzzy", W/"r2d2xxxx", W/"c3piozzzz"
```

``` html
If-None-Match: *
```

## Related specifications

[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.2)
:

