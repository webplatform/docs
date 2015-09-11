---
title: Digest
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
## <span>Summary</span>

Indicates the hash/digest of the full resource, before partial content or encodings.

## <span>Overview table</span>

Direction
:   Response

Features
:

## <span>Syntax</span>

    Digest = "Digest" ":" #(instance-digest)
    instance-digest = digest-algorithm "=" <encoded digest output>

## <span>Examples</span>

```
Digest: SHA=thvDyvhfIqlvFe+A9MYgxAfm1q5=,unixsum=30637
```

## <span>Related specifications</span>

[RFC 3230: Instance Digests in HTTP](http://tools.ietf.org/html/rfc3230)
:

## <span>See also</span>

### <span>Other articles</span>

-   [Want-Digest](/w/index.php?title=http/headers/Want-Digest&action=edit&redlink=1)
