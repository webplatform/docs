---
title: title
tags:
  - API
  - Object
  - Properties
readiness: 'Almost Ready'
standardization_status: 'W3C Last Call Working Draft'
notes:
  - 'Final review.'
summary: 'Gets or sets the title of a Document. When the document is the main document that is shown (meaning, not of an iframe), this is usually shown to the user.'
uri: dom/Document/title

---
# title

## Summary

Gets or sets the title of a Document. When the document is the main document that is shown (meaning, not of an iframe), this is usually shown to the user.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var documentTitle = document.title;
document.title = newDocumentTitle;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The current title of the document.

## Examples

The following script gets the title of the document, changes the first "r" to a "t" (if there is an "r") and sets the result as the title of the document.

``` {.js}
// Getting the title of the document, replacing the first "r"
// with "t" and setting the result as the title of the document.
document.title = document.title.replace("r", "t");
```

## Usage

     Use this property to get or set the title of the document.

## Notes

When [document](/dom/Document) is the main document that is shown to the user, most browsers show the value of this property to the user as the title of the window or page.

## Related specifications

Specification
:   Status
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/dom.html#document.title)
:   Living Standard
[HTML5](http://www.w3.org/TR/html5/dom.html#document.title)
:   W3C Last Call Working Draft

