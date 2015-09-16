---
title: 'ShadowRoot'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The ShadowRoot object is the point of entry to a shadow tree, which provides functional encapsulation of DOM objects within an established document.'
tags:
  0: API
  1: Objects
  3: DOM
  4: Shadow
uri: dom/shadowdom/ShadowRoot

---
## Summary

The ShadowRoot object is the point of entry to a shadow tree, which provides functional encapsulation of DOM objects within an established document.

## Properties

API Name
:   Summary

[activeElement](/dom/shadowdom/ShadowRoot/activeElement)
:   Represents the currently focused element in the shadow tree.

[applyAuthorStyles](/dom/shadowdom/ShadowRoot/applyAuthorStyles)
:   Indicates whether the rules in author styles associated with the element's document apply to the shadow tree. If false (default value), the author styles are not applied to the shadow tree. If true, the author styles are applied.

[innerHTML](/dom/shadowdom/ShadowRoot/innerHTML)
:   Represents the markup of the ShadowRoot's contents.

[resetStyleInheritance](/dom/shadowdom/ShadowRoot/resetStyleInheritance)
:   Indicates whether or not the inheritable CSS properties are set to the initial value at the shadow boundary. If false (default value), the properties continue to inherit. If true, the properties are set to initial value.

[styleSheets](/dom/shadowdom/ShadowRoot/styleSheets)
:   Represents the shadow root style sheets.

## Methods

API Name
:   Summary

[addStyleSheet](/dom/shadowdom/ShadowRoot/addStyleSheet)
:   Adds a new style sheet to shadow root style sheets.

[elementFromPoint](/dom/shadowdom/ShadowRoot/elementFromPoint)
:   Returns an element at specified coordinates.

[getElementById](/dom/shadowdom/ShadowRoot/getElementById)
:   Just like [Document.getElementById](/dom/Document/getElementById) except that it only works within the scope of this ShadowRoot's shadow tree.

[getElementsByClassName](/dom/shadowdom/ShadowRoot/getElementsByClassName)
:   Just like [Document/getElementsByClassName](/dom/Document/getElementsByClassName) except that it only works within the scope of this ShadowRoot's shadow tree.

[getElementsByTagName](/dom/shadowdom/ShadowRoot/getElementsByTagName)
:   Just like [Document/getElementsByTagName](/dom/Document/getElementsByTagName) except that it only works within the scope of this ShadowRoot's shadow tree.

[getElementsByTagNameNS](/dom/shadowdom/ShadowRoot/getElementsByTagNameNS)
:   Just like [document.getElementsByTagNameNS](/dom/Document/getElementsByTagNameNS) except that it only works within the scope of this ShadowRoot's shadow tree.

[getSelection](/dom/shadowdom/ShadowRoot/getSelection)
:   Returns the current selection in this ShadowRoot's shadow tree.

[removeStyleSheet](/dom/shadowdom/ShadowRoot/removeStyleSheet)
:   Removes a style sheet from the ShadowRoot.

## Events

*No events.*

## Related specifications

[Shadow DOM](https://dvcs.w3.org/hg/webcomponents/raw-file/tip/spec/shadow/index.html#dfn-shadow-root)
:   Editor's Draft

## See also

### Related articles

#### Web Components

-   [register](/dom/Document/register)

-   [shadowdom](/dom/shadowdom)

-   [is](/html/attributes/is)

-   [reset-style-inheritance](/html/attributes/reset-style-inheritance)

-   [content](/html/elements/content)

-   [element](/html/elements/element)

-   [template](/html/elements/template)
