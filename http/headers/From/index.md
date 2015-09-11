---
title: From
overview_table:
  Direction: Request
  Features: ''
summary: "Contains an Internet email address for a human user who controls the requesting user agent.\n"
tags:
  - HTTP
  - Headers
uri: http/headers/From

---
## <span>Summary</span>

Contains an Internet email address for a human user who controls the requesting user agent.

Primarily intended for use by robots and spiders so their owners may be contacted if so desired.

## <span>Overview table</span>

Direction
:   Request

Features
:

## <span>Syntax</span>

    From    = mailbox
    mailbox = <mailbox, see [RFC5322], Section 3.4>

## <span>Examples</span>

```
From: webmaster@example.org
```

## <span>Related specifications</span>

[HTTP/1.1 Semantics and Content](http://tools.ietf.org/html/rfc7231#section-5.5.1)
:

