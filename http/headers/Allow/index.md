---
title: 'Allow'
compatibility:
  feature: Allow
  topic: http
overview_table:
  Direction: Response
  Required: 'Along with 405 Method Not allowed'
  Features: ''
summary: 'Lists the methods supported by the target resource.'
tags:
  - HTTP
  - Headers
uri: http/headers/Allow

---
## Summary

Lists the methods supported by the target resource.

## Overview table

Direction
:   Response

Required
:   Along with 405 Method Not allowed

Features
:

## Syntax

    Allow = #method

## Examples

```
Allow: GET, HEAD, PUT
```

```
Allow: GET, HEAD, PUT, DELETE, POST
```

## Usage

     Must be sent in a 405 Method Not Allowed response.

*Should* be sent to an OPTIONS response.

## Related specifications

[RFC7231: HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-7.4.1)
:

