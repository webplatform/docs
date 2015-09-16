---
title: frames
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[frames](https://developer.mozilla.org/en-US/docs/Web/API/Window.frames) Article]'
  - 'Microsoft Developer Network: [[window Object](http://msdn.microsoft.com/en-us/library/ie/ms535873(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Window
summary: 'Returns the window itself, which is an array-like object, listing the direct sub-frames of the current window.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/frames

---
## Summary

Returns the window itself, which is an array-like object, listing the direct sub-frames of the current window.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

**Note**: This property is read-only.

``` js
var frames = window.frames;
```

## Return Value

Returns an object of type DOM NodeDOM Node

Collection of HTMLWindow objects that are children of the window Node.

## Examples

This example in JScript (compatible with ECMA 262 language specification) shows how to display the URLs of the HTML documents contained in windows created by the **iframe** objects in the document.

``` html
var frm = document.frames;
for (i=0; i < frm.length; i++)
    alert(frm(i).location);
```

This example in JScript shows how to display the name of each window defined by **frame** tags in the parent window of the current document.

``` html
var frm = window.parent.frames;
for (i=0; i < frm.length; i++)
    alert(frm(i).name);
```

## Notes

### Remarks

If the HTML source document contains a **body** tag, the collection contains one window for each **iframe** object in the document. If the source document contains **frameSet** tags, the collection contains one window for each **frame** tag in the document. In both cases, the order is determined by the HTML source. This collection contains only **window** objects and does not provide access to the corresponding **frame** and **iframe** objects. Although you can use names with the [**item**](/dom/Element/item) method on this collection, the method never returns a collection. Instead, it always returns the first window having the given name. To ensure that all windows are accessible, make sure that no two windows in a document have the same name.
