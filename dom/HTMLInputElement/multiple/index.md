---
title: multiple
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLInputElement
    href: /dom/HTMLInputElement
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/HTMLInputElement
standardization_status: 'W3C Working Draft'
summary: 'Gets whether a file upload element can be populated with more than a single file.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLInputElement/multiple

---
## <span>Summary</span>

Gets whether a file upload element can be populated with more than a single file.

Property of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## <span>Syntax</span>

``` js
var multipleFiles = inputElement.multiple;
inputElement.multiple = newMultiple;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether multiple files can be populated within the element.

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
