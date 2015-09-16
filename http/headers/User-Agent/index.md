---
title: User-Agent
overview_table:
  Direction: Request
  Features: ''
summary: 'Contains information about the user agent originating the request.'
tags:
  - HTTP
  - Headers
uri: http/headers/User-Agent

---
## Summary

Contains information about the user agent originating the request.

## Overview table

Direction
:   Request

Features
:

## Syntax

    User-Agent = product *( RWS ( product / comment ) )
    product = token ["/" product-version]
    product-version = token

## Examples

```
User-Agent: CERN-LineMode/2.15 libwww/2.17b3
```

Chromium 38 on Linux, showing a proliferation of other user agents it is "also compatible with", a practice common among modern Web browsers

```
User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/38.0.2125.101 Safari/537.36
```

## Related specifications

[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-5.5.3)
:

