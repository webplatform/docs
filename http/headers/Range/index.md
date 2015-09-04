---
title: Range
tags:
  - HTTP
  - Headers
summary: 'The "Range" header field on a GET request modifies the method semantics to request transfer of only one or more subranges of the selected representation data, rather than the entire selected representation data.'
uri: http/headers/Range

---
# Range

## Summary

The "Range" header field on a GET request modifies the method semantics to request transfer of only one or more subranges of the selected representation data, rather than the entire selected representation data.

## Overview table

Direction
:   Request
Features
:

## Syntax

    Range = byte-ranges-specifier / other-ranges-specifier
    byte-ranges-specifier = bytes-unit "=" byte-range-set
    bytes-unit = "bytes"
    byte-range-set  = 1#( byte-range-spec / suffix-byte-range-spec )
    other-ranges-specifier = other-range-unit "=" other-range-set
    other-range-set = 1*VCHAR
    byte-range-spec = first-byte-pos "-" [ last-byte-pos ]
    suffix-byte-range-spec = "-" suffix-length

## Examples

``` {.other}
Range: bytes=0-499
```

    Range: bytes=0-499,1000-1499

## Related specifications

Specification
:   Status
[RFC7233: HTTP/1.1 Range Requests](http://tools.ietf.org/html/rfc7233#section-3.1)
:

