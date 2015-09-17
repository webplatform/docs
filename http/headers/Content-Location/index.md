---
title: 'Content-Location'
compatibility:
  feature: Content-Location
  topic: http
overview_table:
  Direction: 'Request and Response'
  Features: ''
summary: 'References a URI that can be used as an identifier for a specific resource corresponding to the representation in this message''s payload.'
tags:
  - HTTP_Headers
uri: http/headers/Content-Location

---
## Summary

References a URI that can be used as an identifier for a specific resource corresponding to the representation in this message's payload.

## Overview table

Direction
:   Request and Response

Features
:

## Syntax

    Content-Location = absolute-URI / partial-URI

## Examples

```
Content-Location: /images/car.png
```

## Related specifications

[RFC7231: HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-3.1.4.2)
:

