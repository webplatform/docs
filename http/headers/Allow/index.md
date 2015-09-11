---
title: Allow
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
## <span>Summary</span>

Lists the methods supported by the target resource.

## <span>Overview table</span>

Direction
:   Response

Required
:   Along with 405 Method Not allowed

Features
:

## <span>Syntax</span>

    Allow = #method

## <span>Examples</span>

```
Allow: GET, HEAD, PUT
```

```
Allow: GET, HEAD, PUT, DELETE, POST
```

## <span>Usage</span>

     Must be sent in a 405 Method Not Allowed response.

*Should* be sent to an OPTIONS response.

## <span>Related specifications</span>

[RFC7231: HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-7.4.1)
:

