---
title: details
tags:
  - Markup
  - Elements
standardization_status: 'W3C Working Draft'
summary: 'The details element represents a disclosure widget from which the user can obtain additional information or controls.'
code_samples:
  - 'http://gist.github.com/37f1ab4ad9cfb23eaa3d'
uri: html/elements/details
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLDetailsElement

---
# details

## Summary

The details element represents a disclosure widget from which the user can obtain additional information or controls.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLDetailsElement](/w/index.php?title=dom/HTMLDetailsElement&action=edit&redlink=1)

## Attributes

### open

If the `open` attribute is set on the `details` tag, it will be open when it's rendered.

## Browser support

The \<details\> tag is currently only supported in Chrome and in Safari on Mac.

## Examples

``` {.html}
<details open="open">
    <p>Foo</p>
    <p>Bar</p>
    <p>Peter</p>
</details>
```

[View live example](http://code.webplatform.org/gist/37f1ab4ad9cfb23eaa3d)

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/interactive-elements.html#the-details-element)
:   W3C Working Draft

