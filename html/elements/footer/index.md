---
title: footer
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
  - 'Facebook HTML5 Resource Center.'
notes:
  - 'Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The footer element (&lt;footer&gt;) represents content of the end of the nearest ancestor sectioning content or sectioning root element.'
tags:
  - Markup
  - Elements
  - Design
  - HTML
uri: html/elements/footer

---
## Summary

The footer element (&lt;footer&gt;) represents content of the end of the nearest ancestor sectioning content or sectioning root element.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

The basic motivation for introducing the footer element in HTML5 was to eliminate the overuse of [\<div\>](/html/elements/div) elements and creating a suitable element for the links and text that are usually located at the bottom of the webpages.

## Examples

The following example defines two footers, one at the top and one at the bottom, with the same content.

``` html
<body>
 <!-- First footer -->
 <footer><a href="../">Back to index...</a></footer>
 <h1>Lorem ipsum</h1>
 <p>Insert long article here.</p>
 <!-- Second footer -->
 <footer><a href="../">Back to index...</a></footer>
</body>
```

## Notes

### Remarks

Footers don't necessarily have to appear at the end of a section, though they usually do. The **footer** element can contain entire sections to represent appendices, indexes, license agreements, and similar content. Footers might also contain **nav** elements or contact information for the author or editor inside an **address** element. When the nearest ancestor element is the **body** element, then the footer applies to the whole document. The **footer** element is not sectioning content; it does not introduce a new section. Windows Internet Explorer 9. The **footer** element is only supported for webpages displayed in IE9 Standards mode. For more information, see Defining Document Compatibility.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-footer-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/sections.html#the-footer-element)
:   W3C Recommendation

## See also

### Related articles

#### Document Structure

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   **footer**

-   [head](/html/elements/head)

-   [main](/html/elements/main)

-   [nav](/html/elements/nav)

-   [p](/html/elements/p)

-   [section](/html/elements/section)

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

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   **footer**

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

### Related pages

-   `Reference`
-   `article`
-   `aside`
-   `figcaption`
-   `figure`
-   `header`
-   `hgroup`
-   `mark`
-   `nav`
-   `section`
