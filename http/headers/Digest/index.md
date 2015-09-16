---
title: 'Digest'
compatibility:
  feature: Digest
  topic: http
overview_table:
  Direction: Response
  Features: ''
summary: 'Indicates the hash/digest of the full resource, before partial content or encodings.'
tags:
  - HTTP
  - Headers
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - http/headers/Want-Digest
uri: http/headers/Digest

---
## Summary

Indicates the hash/digest of the full resource, before partial content or encodings.

## Overview table

Direction
:   Response

Features
:

## Syntax

    Digest = "Digest" ":" #(instance-digest)
    instance-digest = digest-algorithm "=" <encoded digest output>

## Examples

```
Digest: SHA=thvDyvhfIqlvFe+A9MYgxAfm1q5=,unixsum=30637
```

## Related specifications

[RFC 3230: Instance Digests in HTTP](http://tools.ietf.org/html/rfc3230)
:

## See also

### Other articles

-   [Want-Digest](/w/index.php?title=http/headers/Want-Digest&action=edit&redlink=1)
