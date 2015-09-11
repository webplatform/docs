---
title: title
notes:
  - 'Final review.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: 'W3C Last Call Working Draft'
summary: 'Gets or sets the title of a Document. When the document is the main document that is shown (meaning, not of an iframe), this is usually shown to the user.'
tags:
  - API
  - Object
  - Properties
uri: dom/Document/title

---
## <span>Summary</span>

Gets or sets the title of a Document. When the document is the main document that is shown (meaning, not of an iframe), this is usually shown to the user.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var documentTitle = document.title;
document.title = newDocumentTitle;
```

## <span>Return Value</span>

Returns an object of type StringString

The current title of the document.

## <span>Examples</span>

The following script gets the title of the document, changes the first "r" to a "t" (if there is an "r") and sets the result as the title of the document.

``` js
// Getting the title of the document, replacing the first "r"
// with "t" and setting the result as the title of the document.
document.title = document.title.replace("r", "t");
```

## <span>Usage</span>

     Use this property to get or set the title of the document.

## <span>Notes</span>

When [document](/dom/Document) is the main document that is shown to the user, most browsers show the value of this property to the user as the title of the window or page.

## <span>Related specifications</span>

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/dom.html#document.title)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5/dom.html#document.title)
:   W3C Last Call Working Draft

