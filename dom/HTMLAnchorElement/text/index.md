---
title: text
notes:
  - 'Final review.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLAnchorElement
    href: /dom/HTMLAnchorElement
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/HTMLAnchorElement
standardization_status: 'W3C Last Call Working Draft'
summary: 'Legacy. Use anchorElement.textContent instead. Functions identically to Node.textContent.'
tags:
  - API
  - Object
  - Properties
uri: dom/HTMLAnchorElement/text

---
## <span>Summary</span>

Legacy. Use anchorElement.textContent instead. Functions identically to Node.textContent.

Property of [dom/HTMLAnchorElement](/dom/HTMLAnchorElement)[dom/HTMLAnchorElement](/dom/HTMLAnchorElement)

## <span>Syntax</span>

``` js
var anchorText = anchorElement.text;
anchorElement.text = newAnchorText;
```

## <span>Return Value</span>

Returns an object of type StringString

The text content of the element.

## <span>Examples</span>

The following script replaces every instance of the letter "a" in the text of an [**a**](/html/elements/a) element with instances of the letter "t", using the **text** property for getting and setting the text.

``` js
// Caching the a element for further use.
var anchor = document.getElementById("some-anchor");
// Getting the text of the element, replacing
// any "a" with "t" using a regular expression
// and setting the result back to the text property.
// Alternatively,
// use anchor.textContent = anchor.textContent.replace(/a/g, "t"); instead.
anchor.text = anchor.text.replace(/a/g, "t");
```

## <span>Related specifications</span>

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html#dom-a-text)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5/text-level-semantics.html#dom-a-text)
:   W3C Last Call Working Draft

