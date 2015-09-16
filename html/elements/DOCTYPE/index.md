---
title: '!DOCTYPE'
compatibility:
  feature: '!DOCTYPE'
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
summary: 'A Document Type Declaration, or DOCTYPE, is an instruction that associates a particular SGML or XML document (for example, a webpage) with a Document Type Definition (DTD) (for example, the formal definition of a particular version of HTML). In the serialized form of the document, it manifests as a short string of markup that conforms to a particular syntax. Not including &lt;!DOCTYPE&gt; may trigger Quirks mode.'
tags:
  - Markup
  - Elements
  - DOCTYPE
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - SGML
    - XML
    - webpage
    - 'Document Type Definition'
    - HTML
    - Serialization
    - 'Markup language'
    - 'html/Quirks mode'
    - HTML5
uri: html/elements/!DOCTYPE

---
## Summary

A Document Type Declaration, or DOCTYPE, is an instruction that associates a particular SGML or XML document (for example, a webpage) with a Document Type Definition (DTD) (for example, the formal definition of a particular version of HTML). In the serialized form of the document, it manifests as a short string of markup that conforms to a particular syntax. Not including &lt;!DOCTYPE&gt; may trigger Quirks mode.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

HTML5 has one doctype declaration

``` html
<!DOCTYPE html>
```

HTML 4.01 Strict

``` html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
```

HTML 4.01 Transitional

``` html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

## Usage

     Add

``` html
<!DOCTYPE html>
```

    to the start of your document.

## Notes

The \<!DOCTYPE\> declaration must be the very first thing in an HTML document, before the \<html\> tag.

This is not a HTML tag but an instruction for the browser about the version of the document.

In HTML 4.01, the \<!DOCTYPE\> declaration refers to a DTD, because HTML 4.01 was based on SGML. The DTD specifies the rules for the markup language, so that the browsers render the content correctly.

[HTML5](/w/index.php?title=HTML5&action=edit&redlink=1) is not based on SGML, and therefore does not require a reference to a DTD.

## See also

### Related articles

#### Deprecated

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)

-   [MutationEvent](/dom/MutationEvent)

-   [attrChange](/dom/MutationEvent/attrChange)

-   [attrName](/dom/MutationEvent/attrName)

-   [initMutationEvent](/dom/MutationEvent/initMutationEvent)

-   [newValue](/dom/MutationEvent/newValue)

-   [prevValue](/dom/MutationEvent/prevValue)

-   [relatedNode](/dom/MutationEvent/relatedNode)

-   **!DOCTYPE**

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [escape](/javascript/escape)

-   [unescape](/javascript/unescape)

#### HTML

-   [user-modify](/css/properties/user-modify)

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

-   **!DOCTYPE**

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

-   [datalist](/html/elements/datalist)

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

-   [html](/html/elements/html)

-   [i](/html/elements/i)

-   [img](/html/elements/img)

-   [input](/html/elements/input)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [legend](/html/elements/legend)

-   [mark](/html/elements/mark)

-   [option](/html/elements/option)

-   [p](/html/elements/p)

-   [samp](/html/elements/samp)

-   [script](/html/elements/script)

-   [span](/html/elements/span)

-   [strong](/html/elements/strong)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

### Other articles

html/quirksmode
