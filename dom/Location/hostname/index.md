---
title: hostname
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary, examples, compatibility, standards, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Location
    href: /dom/Location
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Location
summary: 'Sets or retrieves the host name part of the location or URL.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Location/hostname

---
## Summary

Sets or retrieves the host name part of the location or URL.

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## Syntax

``` js
var hostName = location.hostname;
location.hostname = hostName;
```

## Return Value

Returns an object of type StringString

The host name component of the URL.

**Needs Examples**: This section should include examples.

## Notes

If no host name is available, this property returns an empty string.
