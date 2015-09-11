---
title: code
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
  0: API
  1: Object
  2: Properties
  4: Audio
  5: DOM
  6: Video
uri: dom/HTMLMediaError/code

---
## <span>Summary</span>

Returns the current HTMLMediaError code or null if no error has occurred.

Property of [dom/HTMLMediaError](/dom/HTMLMediaError)[dom/HTMLMediaError](/dom/HTMLMediaError)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var errorCode = audio.error.code;
```

## <span>Return Value</span>

Returns an object of type unsigned shortunsigned short

The error code (from the [MediaError](/dom/HTMLMediaError) constants), or null.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

If no error has occurred, the [**MediaError**](/dom/HTMLMediaError) object is null.

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
