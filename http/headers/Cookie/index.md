---
title: Cookie
notes:
  - "* Details on when to use (or rather, when **not** to use) cookies\n Security concerns with using for authenticating users, background on CSRF"
overview_table:
  Direction: Request
  Features: ''
standardization_status: Mixed
summary: "The Cookie headers may be used to receive the value of a cookie from a user agent. The value of the cookie will have been previously set though a script, or by the Set-Cookie header.\n"
tags:
  - HTTP
  - Headers
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - http/headers/Set-Cookie
uri: http/headers/Cookie

---
## <span>Summary</span>

The Cookie headers may be used to receive the value of a cookie from a user agent. The value of the cookie will have been previously set though a script, or by the Set-Cookie header.

Cookies have many issues associated with them, including security and CSRF attacks, privacy issues, and a nonstandard format compared to other HTTP headers.

## <span>Overview table</span>

Direction
:   Request

Features
:

## <span>Syntax</span>

    cookie-header = "Cookie:" OWS cookie-string OWS
    cookie-string = cookie-pair *( ";" SP cookie-pair )
    cookie-pair       = cookie-name "=" cookie-value
    cookie-name       = token
    cookie-value      = *cookie-octet / ( DQUOTE *cookie-octet DQUOTE )
    cookie-octet      = %x21 / %x23-2B / %x2D-3A / %x3C-5B / %x5D-7E
                           ; US-ASCII characters excluding CTLs,
                           ; whitespace DQUOTE, comma, semicolon,
                           ; and backslash

## <span>Examples</span>

A user agent sending a cookie named "SID" with the value "31d4d96e407aad42".

```
Cookie: SID=31d4d96e407aad42
```

## <span>Related specifications</span>

[HTTP State Management Mechanism](http://tools.ietf.org/html/rfc6265)
:

