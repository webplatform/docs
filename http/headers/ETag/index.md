---
title: ETag
tags:
  - HTTP
  - Headers
summary: 'Provides the entity-tag for the current selected representation, an opaque token that varies over revisions and representations.'
uri: http/headers/ETag

---
# ETag

## Summary

Provides the entity-tag for the current selected representation, an opaque token that varies over revisions and representations.

## Overview table

Direction
:   Response
Features
:

## Syntax

    ETag       = entity-tag
    entity-tag = [ weak ] opaque-tag
    weak       = %x57.2F ; "W/", case-sensitive
    opaque-tag = DQUOTE *etagc DQUOTE
    etagc      = %x21 / %x23-7E / obs-text ; VCHAR except double quotes, plus obs-text

## Examples

    ETag: "xyzzy"

    ETag: W/"xyzzy"

    ETag: ""

## Usage

     ETag is defined as a validator header field, and as such conveys information about the selected representation. In safe responses (GET, HEAD), this will provide metadata about the attached response. In unsafe responses (PUT, PATCH, POST, DELETE), the header describes the new resource that has replaced the old one (if any), and the server must not send the header if the resource has been altered or normalized in any way.

## Related specifications

Specification
:   Status
[RFC7232: HTTP/1.1 Conditional Requests](http://tools.ietf.org/html/rfc7232#section-2.3)
:

