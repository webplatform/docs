---
title: Content-Location
overview_table:
  Direction: 'Request and Response'
  Features: ''
summary: 'References a URI that can be used as an identifier for a specific resource corresponding to the representation in this message''s payload.'
tags:
  - HTTP
  - Headers
uri: http/headers/Content-Location

---
## <span>Summary</span>

References a URI that can be used as an identifier for a specific resource corresponding to the representation in this message's payload.

## <span>Overview table</span>

Direction
:   Request and Response

Features
:

## <span>Syntax</span>

    Content-Location = absolute-URI / partial-URI

## <span>Examples</span>

```
Content-Location: /images/car.png
```

## <span>Related specifications</span>

[RFC7231: HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-3.1.4.2)
:

