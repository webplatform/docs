---
title: If-None-Match
tags:
  - HTTP
  - Headers
summary: 'Makes a request conditional on a resource having changed from the specified ETag (version or representation), for refreshing caches.'
uri: http/headers/If-None-Match

---
# If-None-Match

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

    If-None-Match: "xyzzy"

    If-None-Match: W/"xyzzy", W/"r2d2xxxx", W/"c3piozzzz"

    If-None-Match: *

## Related specifications

Specification
:   Status
[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.2)
:

