---
title: 'From'
compatibility:
  feature: From
  topic: http
overview_table:
  Direction: Request
  Features: ''
summary: "Contains an Internet email address for a human user who controls the requesting user agent.\n"
tags:
  - HTTP_Headers
uri: http/headers/From

---
## Summary

Contains an Internet email address for a human user who controls the requesting user agent.

Primarily intended for use by robots and spiders so their owners may be contacted if so desired.

## Overview table

Direction
:   Request

Features
:

## Syntax

    From    = mailbox
    mailbox = <mailbox, see [RFC5322], Section 3.4>

## Examples

```
From: webmaster@example.org
```

## Related specifications

[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-5.5.1)
:

