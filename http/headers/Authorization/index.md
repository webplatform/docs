---
title: Authorization
tags:
  - HTTP
  - Headers
summary: 'Allows a user agent to authenticate itself with an origin server.'
uri: http/headers/Authorization

---
# Authorization

## Summary

Allows a user agent to authenticate itself with an origin server.

## Overview table

Direction
:
Features
:

## Syntax

    Authorization = credentials
    credentials = auth-scheme [ 1*SP ( token68 / #auth-param ) ]
    auth-scheme = token
    auth-param = token BWS "=" BWS ( token / quoted-string )
    token68 = 1*( ALPHA / DIGIT /  "-" / "." / "_" / "~" / "+" / "/" ) *"="

## Examples

``` {.other}
Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==
```

## Notes

Other specifications define the authorization schemes that may be used with the header: A registry of these Authorization schemes is maintained by the IANA in the [Hypertext Transfer Protocol (HTTP) Authentication Scheme Registry](http://www.iana.org/assignments/http-authschemes/http-authschemes.xhtml).

## Related specifications

Specification
:   Status
[RFC7235: HTTP/1.1 Authentication](http://tools.ietf.org/html/rfc7235#section-4.2)
:

