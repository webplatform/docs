---
title: If-Range
tags:
  - HTTP
  - Headers
summary: 'Asks the server to apply the range request only if the provided ETag or Last-Modified date is current; otherwise send the entire resource.'
uri: http/headers/If-Range

---
# If-Range

## Summary

Asks the server to apply the range request only if the provided ETag or Last-Modified date is current; otherwise send the entire resource.

## Overview table

Direction
:   Request
Features
:

## Syntax

    If-Range = entity-tag / HTTP-date

**Needs Examples**: This section should include examples.

## Usage

     A client MUST NOT generate an If-Range header field containing an entity-tag that is marked as weak.

A client MUST NOT generate an If-Range header field containing an HTTP-date unless the client has no entity-tag for the corresponding representation and the date is a strong validator in the sense defined by [Section 2.2.2 of RFC7232](http://tools.ietf.org/html/rfc7232#section-2.2.2).

## Related specifications

Specification
:   Status
[RFC7233: HTTP/1.1 Range Requests](http://tools.ietf.org/html/rfc7233#section-3.2)
:

