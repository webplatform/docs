---
title: If-Unmodified-Since
tags:
  - HTTP
  - Headers
summary: 'Makes a request conditional on having a certain last-modified timestamp, used to prevent "lost updates" when modifying resources.'
uri: http/headers/If-Unmodified-Since

---
# If-Unmodified-Since

## Summary

Makes a request conditional on having a certain last-modified timestamp, used to prevent "lost updates" when modifying resources.

## Overview table

Direction
:   Request
Features
:

## Syntax

    If-Unmodified-Since = HTTP-date

## Examples

    If-Unmodified-Since: Sat, 29 Oct 1994 19:43:31 GMT

## Related specifications

Specification
:   Status
[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-3.4)
:

