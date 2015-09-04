---
title: text
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Last Call Working Draft'
notes:
  - 'Final review.'
summary: 'Legacy. Use document.title instead. When setting, does same as textContent. When getting, gets a concatenated version of all of the child text nodes of a title element.'
uri: dom/HTMLTitleElement/text

---
# text

## Summary

Legacy. Use document.title instead. When setting, does same as textContent. When getting, gets a concatenated version of all of the child text nodes of a title element.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLTitleElement](/dom/HTMLTitleElement)</span></span>

## Syntax

``` {.js}
var titleText = titleElement.text;
titleElement.text = newTitleText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

A concatenation of all of the child [text nodes](/dom/Text) of the element.

## Examples

The following script gets the text of the title element, changes "r" to "t" and sets the text back.

``` {.js}
// Note - this example assumes that this script runs
// after the title element is created.

// Caching the first title element in the document for further use.
var title = document.getElementsByTagName("title")[0];
// Getting the text of the element, replacing the first "r"
// with "t" and setting the result back to the text property.
// Alternatively,
// use document.title = document.title.replace("r", "t"); instead.
title.text = title.text.replace("r", "t");
```

## Usage

     Legacy. Use document.title instead.

Use this property to get a concatenated version of all of the child text nodes of a [title](/html/elements/title) element. Setting this property works the same way as setting the [textContent](/dom/Node/textContent) property.

## Notes

-   [Text nodes](/dom/Text) that are nested within elements or HTML comments are excluded.

## Related specifications

Specification
:   Status
[Document Object Model (DOM) Level 1](http://www.w3.org/TR/REC-DOM-Level-1/level-one-html.html#ID-77500413)
:   W3C Recommendation
[Document Object Model (DOM) Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-77500413)
:   W3C Recommendation
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html#dom-title-text)
:   Living Standard
[HTML5](http://www.w3.org/TR/html5/text-level-semantics.html#dom-a-text)
:   W3C Last Call Working Draft

