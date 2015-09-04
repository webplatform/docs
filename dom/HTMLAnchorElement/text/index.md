---
title: text
tags:
  - API
  - Object
  - Properties
readiness: 'Almost Ready'
standardization_status: 'W3C Last Call Working Draft'
notes:
  - 'Final review.'
summary: 'Legacy. Use anchorElement.textContent instead. Functions identically to Node.textContent.'
uri: dom/HTMLAnchorElement/text

---
# text

## Summary

Legacy. Use anchorElement.textContent instead. Functions identically to Node.textContent.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLAnchorElement](/dom/HTMLAnchorElement)</span></span>

## Syntax

``` {.js}
var anchorText = anchorElement.text;
anchorElement.text = newAnchorText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The text content of the element.

## Examples

The following script replaces every instance of the letter "a" in the text of an [**a**](/html/elements/a) element with instances of the letter "t", using the **text** property for getting and setting the text.

``` {.js}
// Caching the a element for further use.
var anchor = document.getElementById("some-anchor");
// Getting the text of the element, replacing
// any "a" with "t" using a regular expression
// and setting the result back to the text property.
// Alternatively,
// use anchor.textContent = anchor.textContent.replace(/a/g, "t"); instead.
anchor.text = anchor.text.replace(/a/g, "t");
```

## Related specifications

Specification
:   Status
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html#dom-a-text)
:   Living Standard
[HTML5](http://www.w3.org/TR/html5/text-level-semantics.html#dom-a-text)
:   W3C Last Call Working Draft

