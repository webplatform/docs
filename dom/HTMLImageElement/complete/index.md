---
title: complete
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'examples, clean-up of MSDN import'
summary: 'Gets whether an image is completely loaded.'
uri: dom/HTMLImageElement/complete
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/naturalWidth
    - dom/properties/naturalHeight

---
# complete

## Summary

Gets whether an image is completely loaded.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLImageElement](/dom/HTMLImageElement)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var complete = image.complete;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the image is completely loaded.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to determine whether an image is completely loaded, or still in the process of loading.

## Notes

Once an image is completely loaded, you can get its actual [naturalWidth](/w/index.php?title=dom/properties/naturalWidth&action=edit&redlink=1) and [naturalHeight](/w/index.php?title=dom/properties/naturalHeight&action=edit&redlink=1) properties, or make layout assumptions.

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## See also

### Related pages (MSDN)

-   `img`
-   `input`
-   `input type=image`
-   `Reference`
-   `onreadystatechange`
-   `readyState`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

