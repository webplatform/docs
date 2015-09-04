---
title: is
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Describes the base element from which the element with this attribute is extended.'
uri: html/attributes/is
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/document/createElement

---
# is

## Summary

Describes the base element from which the element with this attribute is extended.

Applies to
:   dom/HTMLElement

Extending an element with [document.createElement](/w/index.php?title=dom/document/createElement&action=edit&redlink=1) creates a new element. To use that element in markup, you must describe the element with a tag and include the `is=` attribute with the value of the base element from which the new element is extended. See examples.

## Examples

Markup for an extended element.

``` {.html}
<button is="mega-button">
```

Creates the custom element 'mega-button', which is extended from the 'button' element.

``` {.js}
var megaButton = document.createElement('button', 'mega-button');
// megaButton instanceof MegaButton === true
```

## Usage

     The extended element name must contain at least one dash (-). So for example, <x-foo>, <foo-element>, and <my-foo-element> are valid names, while <tabs> and <foo_bar> are not.

## Notes

The custom element name must not be one of the following existing hyphen-containing element names:

-   annotation-xml
-   color-profile
-   font-face
-   font-face-src
-   font-face-uri
-   font-face-format
-   font-face-name
-   missing-glyph

## Related specifications

Specification
:   Status
[Custom Elements](https://dvcs.w3.org/hg/webcomponents/raw-file/tip/spec/custom/index.html)
:   Working draft

## See also

### Related articles

#### Web Components

-   [register](/dom/Document/register)

-   [shadowdom](/dom/shadowdom)

-   [ShadowRoot](/dom/shadowdom/ShadowRoot)

-   **is**

-   [reset-style-inheritance](/html/attributes/reset-style-inheritance)

-   [content](/html/elements/content)

-   [element](/html/elements/element)

-   [template](/html/elements/template)

### External resources

See [Custom Elements](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/) on [HTML5Rocks!](http://www.html5rocks.com).

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from HTML5Rocks! [Custom Elements article](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/)

