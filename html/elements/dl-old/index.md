---
title: 'dl – description list'
code_samples:
  - 'http://code.webplatform.org/gist/5821157'
notes:
  - 'Deletion Candidate'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;dl&gt; element is used to define a description list. The element encloses one or more description terms, enclosed in &lt;dt&gt; elements, and description definitions (definitions of the terms), enclosed within &lt;dd&gt; elements.'
tags:
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/concepts/flowContent
uri: html/elements/dl-old

---
## Summary

The &lt;dl&gt; element is used to define a description list. The element encloses one or more description terms, enclosed in &lt;dt&gt; elements, and description definitions (definitions of the terms), enclosed within &lt;dd&gt; elements.

<table class="wikitable">
<tr>
<th style="vertical-align: top" id="permitted-contents">
Permitted contents

</th>
<td style="vertical-align: top; padding-top: 10px">
One of the following:

-   Either: Zero or more groups each consisting of one or more [`<dt>`](/html/elements/dt) elements followed by one or more [`<dd>`](/html/elements/dt) elements.
-   Or: A [`<template>`](/html/elements/template) element.
-   Or: A [`<template>`](/html/elements/template) element or a [`<dt>`](/html/elements/dt) element, followed by zero or more [`<template>`](/html/elements/template), [`<dt>`](/html/elements/dt), and [`<dd>`](/html/elements/dd) elements, followed by a [`<template>`](/html/elements/template) element or a [`<dd>`](/html/elements/dd) element.

</td>
</tr>
<tr>
<th id="permitted-parents">
Permitted parents

</th>
<td>
Any element that can contain [flow content](/w/index.php?title=html/concepts/flowContent&action=edit&redlink=1).

</td>
</tr>
<tr>
<th id="tag-omission">
Tag omission

</th>
<td>
A `<dl>` element must have both a start tag and an end tag.

</td>
</tr>
<tr>
<th id="dom-interface">
DOM interface

</th>
<td>
[HTMLDListElement](/dom/HTMLDListElement)

</td>
</tr>
</table>
## Usage

The `<dl>` element is often useful to create a semantic list of terms and their definitions, whether these are name value pairs, glossary terms and definitions, or anything other items that fit this pattern. **Description lists** allow you to do this easily inside HTML.

A description list is always wrapped by a single `<dl>` element. Inside that element you can place any number of child **description items** — the items to be described or defined — inside `<dt>` elements, and **description definitions** — the description or definition of the specified items — inside `<dd>` elements.

It doesn't make sense to have an item without a description, or the other way round, but note that it is acceptable to have a single item with multiple descriptions, or a description with multiple items (see code examples section.)

The items should always be placed before the descriptions.

A description list is not used as commonly as other types of list, except in journals, research papers, and other documentation where item/value pairs need to be displayed. For other uses, they are often not used as they are considered more difficult to style than other list types.

## CSS

Typical browser default CSS properties for the `<dl>` element.

``` css
display: block;
margin-top: 16px;
margin-bottom: 16px;
```

## Examples

Three different description list examples:

-   The first is a simple example with two item/description pairs.
-   The second shows an example with a single item but multiple descriptions for that item.
-   The third shows an example with a single description and multiple items fitting that description.

``` html
<h2>Simple description list</h2>

<dl>
  <dt>Coffee</dt>
  <dd>A popular hot drink.</dd>
  <dt>Coca Cola</dt>
  <dd>One of the leading brands of a popular cold fizzy drink.</dd>
</dl>

<h2>One item, several descriptions</h2>

<dl>
  <dt>Coffee</dt>
  <dd>A popular hot drink.</dd>
  <dd>A mid brown colour</dd>
  <dd>A common social invitation</dd>
</dl>

<h2>One description, several items</h2>

<dl>
  <dt>Coffee</dt>
  <dt>Tea</dt>
  <dt>Vimto (in the North of England)</dt>
  <dd>A popular hot drink.</dd>
</dl>
```

[View live example](http://code.webplatform.org/gist/5821157)

## Related specifications

[HTML5.1](http://www.w3.org/html/wg/drafts/html/master/)
:   Editor's draft

[HTML 4.01](http://www.w3.org/TR/html401/struct/lists.html)
:   W3C Recommendation

## See also

### External resources

-   [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/HTML/Element/dl)
-   [W3C](http://www.w3.org/TR/html4/struct/lists.html#h-10.3)
