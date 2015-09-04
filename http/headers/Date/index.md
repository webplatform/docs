---
title: Date
tags:
  - HTTP
  - Headers
readiness: 'Not Ready'
summary: 'Represents the date and time at which the message was originated.'
uri: http/headers/Date

---
# Date

## Summary

Represents the date and time at which the message was originated.

## Overview table

Direction
:   Request and Response
Required
:   Responses
Features
:   HTTP

## Syntax

    Date = HTTP-date
    HTTP-date = IMF-fixdate / obs-date

## Examples

A simple example to show the effect achieved when small-caps are applied to a text paragraph.

``` {.http .header}
Date: Sun, 06 Nov 1994 08:49:37 GMT
```

## Related specifications

Specification
:   Status
[RFC7231: HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-7.1.1.2)
:   N/A

