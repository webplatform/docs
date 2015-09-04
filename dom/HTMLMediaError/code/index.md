---
title: code
tags:
  0: API
  1: Object
  2: Properties
  4: Audio
  5: DOM
  6: Video
readiness: 'In Progress'
notes:
  - 'examples, clean-up of MSDN import'
summary: 'Returns the current HTMLMediaError code or null if no error has occurred.'
uri: dom/HTMLMediaError/code

---
# code

## Summary

Returns the current HTMLMediaError code or null if no error has occurred.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLMediaError](/dom/HTMLMediaError)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var errorCode = audio.error.code;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

The error code (from the [MediaError](/dom/HTMLMediaError) constants), or null.

**Needs Examples**: This section should include examples.

## Notes

If no error has occurred, the [**MediaError**](/dom/HTMLMediaError) object is null.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

