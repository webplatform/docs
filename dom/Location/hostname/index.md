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
## <span>Summary</span>

Sets or retrieves the host name part of the location or URL.

Property of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## <span>Syntax</span>

``` js
var hostName = location.hostname;
location.hostname = hostName;
```

## <span>Return Value</span>

Returns an object of type StringString

The host name component of the URL.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

If no host name is available, this property returns an empty string.