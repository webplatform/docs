---
title: If-Match
tags:
  - HTTP
  - Headers
summary: 'Makes the request conditional on the server''s resource being a certain ETag (revision and representation).'
uri: http/headers/If-Match

---
# If-Match

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

    If-Match: "xyzzy"

    If-Match: "xyzzy", "r2d2xxxx", "c3piozzzz"

    If-Match: *

## Related specifications

Specification
:   Status
[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.1)
:

