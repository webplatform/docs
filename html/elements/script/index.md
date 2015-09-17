---
title: 'script'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: script
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLScriptElement](/dom/HTMLScriptElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The script element enables dynamic script and data blocks to be included in documents. It can contain code/data directly or it can link to external sources. It is mainly used with JavaScript.'
tags:
  - Markup_Elements
  - HTML
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/attributes/Type
uri: html/elements/script

---
## Summary

The script element enables dynamic script and data blocks to be included in documents. It can contain code/data directly or it can link to external sources. It is mainly used with JavaScript.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLScriptElement](/dom/HTMLScriptElement)

### Attributes

|Property|Description|Used with inline scripts|
|:-------|:----------|:-----------------------|
|[**src**](/html/attributes/src_(script))|The URL to an external file that contains the source code or data.|No|
|[**type**](/html/attributes/type_(script_element))|The MIME type for the script. Required in HTML 4, defaults to `text/javascript` in HTML 5. For JavaScript, this should always be set to `application/javascript` since [RFC4329](https://tools.ietf.org/html/rfc4329).|Yes|
|[**charset**](/html/attributes/charset)|Sets or retrieves the script's character encoding. You can't use the type attribute with this attribute.|No|
|[**language**](/html/attributes/language)|The programming language for the associated scripting engine. Depracated, use type instead.|Yes|
|[**defer**](/html/attributes/defer)|Specifies that script should be executed after the document has been parsed.|No|
|[**async**](/html/attributes/async)|Specifies that the script should be executed asynchronously, as soon as it becomes available.|No|
|[**crossorigin**](/html/attributes/crossorigin)|Whether or not script error information will be revealed from the script(This is used only when scripts are being loaded from different origins).|No|

## Examples

Loading an external script.

``` html
<script src="http://example.com/Script/Url/here.js" type="application/javascript"></script>
```

Writing an inline script.

``` html
<script type="application/javascript">
  //Do stuff...
</script>
```

## Notes

Code within the **script** block that is not contained within a function is executed immediately as the document is loaded.When the [**Type**](/w/index.php?title=html/attributes/Type&action=edit&redlink=1) attribute is unset on the **script** object, then `text/javascript` is used. The order of the **script** objects in a document can also be important, especially if scripting event handlers are assigned to one or more elements in the document. Using `async="async"` didn't work in some older browser, instead `async="true"` was used.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/scripting-1.html#the-script-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/scripting-1.html#the-script-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/scripts.html#edef-SCRIPT)
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

-   **script**

-   [span](/html/elements/span)

-   [strong](/html/elements/strong)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

### Other articles

[\<noscript\> tag](/html/elements/noscript)

### Related pages

-   `XML Data Islands`
