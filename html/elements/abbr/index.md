---
title: 'abbr'
code_samples:
  - 'http://gist.github.com/939206'
compatibility:
  feature: abbr
  topic: html
notes:
  - 'Add syntax, attribute, compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Use the abbr element to indicate an abbreviation or acronym.'
tags:
  - Markup_Elements
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/acronym
uri: html/elements/abbr

---
## Summary

Use the abbr element to indicate an abbreviation or acronym.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

The **abbr** is a phrasing-level element used to indicate an abbreviation or acronym. It can’t contain block-level elements, but it can contain other phrasing type elements.

The **abbr** element’s role has been expanded to incorporate the role previously performed by [**acronym** element](/w/index.php?title=html/acronym&action=edit&redlink=1) (which has been deprecated).

## Attributes

A **abbr** element may optionally have a [**title** attribute](/html/attributes/title) that must contain an expansion of the abbreviation (and nothing else). The **abbr** element can accept any attributes permitted globally (e.g. **class**).

## Examples

The following example shows how to use the **abbr** element with an optional [**title**](/html/attributes/title) attribute.

``` html
<p>The national capital of the
United States is located in Washington,
<abbr title="District of Columbia">D.C.</abbr>.</p>
```

[View live example](http://gist.github.com/939206)

Linking an abbreviation to its definition

``` html
<p>
The <dfn id="HTML">Hyper Text Markup Language</dfn>
(<abbr title="HyperText Markup Language">HTML</abbr>) is the publishing language of the World Wide Web.
</p>
<p>The first version of <a href="#HTML"><abbr title="Hyper Text Markup Language">HTML</abbr></a>
 was described by Tim Berners-Lee in late 1991.</p>
```

## Usage

     Abbreviations don’t have to marked up in the abbr element, but it can be useful

-   When you want to provide an expanded version of the term;
-   When you are using a term that may be unfamiliar to your audience; or
-   When you want to visually-separate abbreviations from other content on the page (using CSS).

In the first two instances, it would make sense to include an expansion of the abbreviation in a **title** attribute.

## Notes

If you use the same abbreviation multiple times in a document, you might consider using a **title** to expand the first instance (perhaps wrapping it in a [**dfn** element](/html/elements/dfn) to mark it as the defining instance) and then leave the **title** attribute off of the additional instances. This may provide a better reading experience for assistive technologies, but it should be noted that the instances without **title** attributes will not provide the expanded text as each **abbr** is independent (expansions are not shared among identical **abbr** elements).

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-abbr-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-abbr-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-ABBR)
:   W3C Recommendation

