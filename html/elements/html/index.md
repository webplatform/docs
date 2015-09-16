---
title: html
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add Category, Parent, Children and Compatibility information. Add HTML information section. Complete Events section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLHtmlElement](/dom/HTMLHtmlElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The html element (&lt;html&gt;) represents the root of an HTML document. The &lt;html&gt; tag is the container for all other HTML elements; except for the &lt;!DOCTYPE&gt; tag.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/html

---
## Summary

The html element (&lt;html&gt;) represents the root of an HTML document. The &lt;html&gt; tag is the container for all other HTML elements; except for the &lt;!DOCTYPE&gt; tag.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLHtmlElement](/dom/HTMLHtmlElement)

The **html** element is used to contain a complete HTML document.

``` html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>An Example Web Page</title>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>
      This is an example web page marked up using HTML.
    </p>
  </body>
</html>
```

Internationalization topics related to the `html` element:

-   [Declaring the overall language of a page](http://www.w3.org/International/techniques/authoring-html#textprocessing)
-   [Setting up a right-to-left page](http://www.w3.org/International/techniques/authoring-html#using)

## Notes

### Remarks

When you use the [!DOCTYPE](/html/elements/!DOCTYPE) declaration to specify standards-compliant mode, this element represents the canvas—the entire surface onto which a document's contents can be rendered. When you switch on standards-compliant mode, this element also becomes the positioning container for positioned elements that don't have a positioned parent. When the !DOCTYPE declaration does not specify standards-compliant mode, the **body** object represents the entire surface onto which a document's contents can be rendered.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/semantics.html#the-html-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/semantics.html#the-html-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-HTML)
:   W3C Recommendation

## See also

### Related articles

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

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

-   **html**

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
