---
title: If-Match
overview_table:
  Direction: Request
  Features: ''
summary: 'Makes the request conditional on the server''s resource being a certain ETag (revision and representation).'
tags:
  - HTTP
  - Headers
uri: http/headers/If-Match

---
## Summary

Makes the request conditional on the server's resource being a certain ETag (revision and representation).

## Overview table

Direction
:   Request

Features
:

## Syntax

    If-Match = "*" / 1#entity-tag

## Examples

``` html
If-Match: "xyzzy"
```

``` html
If-Match: "xyzzy", "r2d2xxxx", "c3piozzzz"
```

``` html
If-Match: *
```

## Related specifications

[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.1)
:

