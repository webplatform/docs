---
title: datalist
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
notes:
  - 'Add Category, Parent and Children information. Complete Compatibility information.'
summary: 'The datalist element (<datalist>) represents a set of <option> elements that represent predefined options for other controls. It may be associated with an <input> element by adding a list attribute to the input element.'
uri: html/elements/datalist
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLDataListElement
    - 'dom/properties/options (dom/options'

---
# datalist

## Summary

The datalist element (\<datalist\>) represents a set of \<option\> elements that represent predefined options for other controls. It may be associated with an \<input\> element by adding a list attribute to the input element.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLDataListElement](/w/index.php?title=dom/HTMLDataListElement&action=edit&redlink=1)

### Attributes

Property
:   Description
[**options**](/w/index.php?title=dom/properties/options_(dom/options&action=edit&redlink=1)
:   A collection of **option** objects that represent possible selections for a **datalist** element.

## Examples

``` {.html}
<input type="text" name="locations" list="places">
<datalist id="places">
     <option>Amman, Jordan</option>
     <option>New York, NY, USA</option>
     <option>Paris, France</option>
     <option>Vienna, Austria</option>
</datalist>
```

Â

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-datalist-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/forms.html#the-datalist-element)
:   W3C Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [HTMLAudioElement](/dom/HTMLAudioElement)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   [HTML Elements](/html/elements)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   **datalist**

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

<!-- -->

    â€¦ further results

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

