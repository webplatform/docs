---
title: Link
tags:
  - HTTP
  - Headers
summary: "Specifies a link between resources, at the HTTP header level.\n"
uri: http/headers/Link

---
# Link

## Summary

Specifies a link between resources, at the HTTP header level.

Carries same semantics as the \<link/\> and \<a/\> tags in HTML.

## Overview table

Direction
:   Request and Response
Features
:

## Syntax

    Link           = "Link" ":" #link-value
    link-value     = "<" URI-Reference ">" *( ";" link-param )
    link-param     = ( ( "rel" "=" relation-types )
                   | ( "anchor" "=" <"> URI-Reference <"> )
                   | ( "rev" "=" relation-types )
                   | ( "hreflang" "=" Language-Tag )
                   | ( "media" "=" ( MediaDesc | ( <"> MediaDesc <"> ) ) )
                   | ( "title" "=" quoted-string )
                   | ( "title*" "=" ext-value )
                   | ( "type" "=" ( media-type | quoted-mt ) )
                   | ( link-extension ) )
    link-extension = ( parmname [ "=" ( ptoken | quoted-string ) ] )
                   | ( ext-name-star "=" ext-value )
    ext-name-star  = parmname "*" ; reserved for RFC2231-profiled
                                  ; extensions.  Whitespace NOT
                                  ; allowed in between.
    ptoken         = 1*ptokenchar
    ptokenchar     = "!" | "#" | "$" | "%" | "&" | "'" | "("
                   | ")" | "*" | "+" | "-" | "." | "/" | DIGIT
                   | ":" | "<" | "=" | ">" | "?" | "@" | ALPHA
                   | "[" | "]" | "^" | "_" | "`" | "{" | "|"
                   | "}" | "~"
    media-type     = type-name "/" subtype-name
    quoted-mt      = <"> media-type <">
    relation-types = relation-type
                   | <"> relation-type *( 1*SP relation-type ) <">
    relation-type  = reg-rel-type | ext-rel-type
    reg-rel-type   = LOALPHA *( LOALPHA | DIGIT | "." | "-" )
    ext-rel-type   = URI

## Examples

    Link: <http://example.com/TheBook/chapter2>; rel="previous"; title="previous chapter"

The Link header carries the same semantics, and many Web browsers recognize this:

    Link: </style/main.css>;rel="stylesheet";type="text/css"

## Related specifications

Specification
:   Status
[RFC5988: Web Linking](http://tools.ietf.org/html/rfc5988)
:

