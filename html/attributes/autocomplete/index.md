---
title: 'autocomplete'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: autocomplete
  topic: html
notes:
  - 'Update/improve example; update descriptions; fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The autocomplete attribute specifies whether a browser should automatically provide values for a form element.'
tags:
  - Markup_Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/input/password
    - html/elements/input/text
uri: html/attributes/autocomplete

---
## Summary

The autocomplete attribute specifies whether a browser should automatically provide values for a form element.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLInputElement](/html/elements/input)

</td>
</tr>
</table>
When autocomplete is on, the browser may automatically fill previously entered values, or match input [names](/html/attributes/name) with values the user has provided.

For sensitive information or form content that is not repeated, autocomplete should be turned off so the user is forced to fill the field every time.

Autocomplete should also be turned off if the website provides its own mechanism for filling a field; for example, an autocomplete like shown in this site's search.

Valid values for autocomplete are `on` or `off`. The attribute is not required.

## Examples

This example uses the **AUTOCOMPLETE** attribute to disable the AutoComplete feature.

``` html
<input type="password" autocomplete="off">
```

The following example shows an HTML form with autocomplete on. One of the inputs ha autocomplete off.

``` html
<form action="submit.php" autocomplete="on">
  First name:<input type="text" name="name"><br />
  Last name: <input type="text" name="surname"><br />
  E-mail: <input type="email" name="email" autocomplete="off"><br />
  <input type="submit">
</form>
```

## Related specifications

[HTML5](http://www.w3.org/TR/html5/forms.html#attr-form-autocomplete)
:   W3C Candidate Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   **autocomplete**

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

-   [script](/html/elements/script)

-   [span](/html/elements/span)

-   [strong](/html/elements/strong)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

#### Security

-   **autocomplete**

### Related pages

-   `input type=password`
-   `input type=text`
-   `form`

[html/elements/input/password](/w/index.php?title=html/elements/input/password&action=edit&redlink=1) [html/elements/input/text](/w/index.php?title=html/elements/input/text&action=edit&redlink=1) [html/elements/form](/html/elements/form)
