---
title: Range
overview_table:
  Direction: Request
  Features: ''
summary: 'The &quot;Range&quot; header field on a GET request modifies the method semantics to request transfer of only one or more subranges of the selected representation data, rather than the entire selected representation data.'
tags:
  - HTTP
  - Headers
uri: http/headers/Range

---
## <span>Summary</span>

The &quot;Range&quot; header field on a GET request modifies the method semantics to request transfer of only one or more subranges of the selected representation data, rather than the entire selected representation data.

## <span>Overview table</span>

Direction
:   Request

Features
:

## <span>Syntax</span>

    Range = byte-ranges-specifier / other-ranges-specifier
    byte-ranges-specifier = bytes-unit "=" byte-range-set
    bytes-unit = "bytes"
    byte-range-set  = 1#( byte-range-spec / suffix-byte-range-spec )
    other-ranges-specifier = other-range-unit "=" other-range-set
    other-range-set = 1*VCHAR
    byte-range-spec = first-byte-pos "-" [ last-byte-pos ]
    suffix-byte-range-spec = "-" suffix-length

## <span>Examples</span>

```
Range: bytes=0-499
```

``` html
Range: bytes=0-499,1000-1499
```

## <span>Related specifications</span>

[RFC7233: HTTP/1.1 Range Requests](http://tools.ietf.org/html/rfc7233#section-3.1)
:

