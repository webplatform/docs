---
title: From
tags:
  - HTTP
  - Headers
summary: "Contains an Internet email address for a human user who controls the requesting user agent.\n"
uri: http/headers/From

---
# From

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

``` {.other}
From: webmaster@example.org
```

## Related specifications

Specification
:   Status
[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-5.5.1)
:

