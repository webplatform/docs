---
title: ID
tags:
  - CSS
  - Selectors
readiness: 'In Progress'
notes:
  - "\nMerge Candidate:  This page is a candidate for merge with the following pages: css/selectors/id_selector \n\n"
summary: 'The #id selector styles the element with the specified id.'
uri: css/selectors/ID
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - selection

---
# ID

## Summary

The \#id selector styles the element with the specified id.

## Examples

The following style rule applies to the element with id="navigation" and its descendants.

    <style>
        #navigation { line-height: 0px; font-size: x-small; }
    </style>

## Notes

### Remarks

The id attribute allows authors to uniquely identify an element instance in the document tree. ID selectors match an element instance based on its identifier. The id attribute value must immediately follow the "pound" (\#) notation. **Note**  Windows Internet Explorer allows multiple elements to share a single ID value. If more than one element exists, the style rule will apply to all elements with the given ID. Only one id attribute may be present on any given element. In the event that a style declaration conflicts with another declaration, the rule with a higher level of specificity is used. (See Understanding CSS Selectors.) If a Class Selector and ID Selector are in conflict, the id is chosen.

### Syntax

`<strong/>sel#value {...}`

### Parameters

*sel*
:   Selector
*value*
:   String that specifies the value of the "id" attribute.

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 1.5

## See also

### Related articles

#### Selectors

-   [querySelectorAll](/css/selectors_api/querySelectorAll)

-   **ID**

-   [Namespaced](/css/selectors/Namespaced)

-   [Universal](/css/selectors/Universal)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [whitespace](/css/selectors/attributes/whitespace)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   [:lang(c)](/css/selectors/pseudo-classes/:lang(c))

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   [:optional](/css/selectors/pseudo-classes/:optional)

-   [:required](/css/selectors/pseudo-classes/:required)

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

-   [::selection](/w/index.php?title=selection&action=edit&redlink=1)

-   [type](/css/selectors/type)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

