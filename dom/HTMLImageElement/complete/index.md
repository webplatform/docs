---
title: 'complete'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLImageElement
    href: /dom/HTMLImageElement
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/HTMLImageElement
summary: 'Gets whether an image is completely loaded.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/naturalWidth
    - dom/properties/naturalHeight
uri: dom/HTMLImageElement/complete

---
## Summary

Gets whether an image is completely loaded.

Property of [dom/HTMLImageElement](/dom/HTMLImageElement)[dom/HTMLImageElement](/dom/HTMLImageElement)

## Syntax

**Note**: This property is read-only.

``` js
var complete = image.complete;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the image is completely loaded.

## Usage

     Use this property to determine whether an image is completely loaded, or still in the process of loading.

## Notes

Once an image is completely loaded, you can get its actual [naturalWidth](/w/index.php?title=dom/properties/naturalWidth&action=edit&redlink=1) and [naturalHeight](/w/index.php?title=dom/properties/naturalHeight&action=edit&redlink=1) properties, or make layout assumptions.

## Related specifications

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## See also

### Related pages

-   `img`
-   `input`
-   `input type=image`
-   `Reference`
-   onreadystatechange[onreadystatechange](/dom/Element/readystatechange)
-   readyState[readyState](/dom/Element/readyState)
