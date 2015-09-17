---
title: 'code'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLMediaError
    href: /dom/HTMLMediaError
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /dom/HTMLMediaError
summary: 'Returns the current HTMLMediaError code or null if no error has occurred.'
tags:
  - API_Object_Properties
  - API
  - Audio
  - DOM
  - Video
  - Needs_Examples
uri: dom/HTMLMediaError/code

---
## Summary

Returns the current HTMLMediaError code or null if no error has occurred.

Property of [dom/HTMLMediaError](/dom/HTMLMediaError)[dom/HTMLMediaError](/dom/HTMLMediaError)

## Syntax

**Note**: This property is read-only.

``` js
var errorCode = audio.error.code;
```

## Return Value

Returns an object of type unsigned shortunsigned short

The error code (from the [MediaError](/dom/HTMLMediaError) constants), or null.

## Notes

If no error has occurred, the [**MediaError**](/dom/HTMLMediaError) object is null.

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
