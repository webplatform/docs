---
title: 'Server'
compatibility:
  feature: Server
  topic: http
overview_table:
  Direction: Response
  Features: ''
summary: 'Contains information about the software used by the origin server to handle the request.'
tags:
  - HTTP
  - Headers
uri: http/headers/Server

---
## Summary

Contains information about the software used by the origin server to handle the request.

## Overview table

Direction
:   Response

Features
:

## Syntax

    Server = product *( RWS ( product / comment ) )
    product = token ["/" product-version]
    product-version = token

## Examples

```
User-Agent: CERN-LineMode/2.15 libwww/2.17b3
```

``` html
Server: Apache/2.2.22 (Debian)
```

## Related specifications

[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-7.4.2)
:

