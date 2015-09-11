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
## <span>Summary</span>

Makes the request conditional on the server's resource being a certain ETag (revision and representation).

## <span>Overview table</span>

Direction
:   Request

Features
:

## <span>Syntax</span>

    If-Match = "*" / 1#entity-tag

## <span>Examples</span>

``` html
If-Match: "xyzzy"
```

``` html
If-Match: "xyzzy", "r2d2xxxx", "c3piozzzz"
```

``` html
If-Match: *
```

## <span>Related specifications</span>

[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.1)
:

