---
title: 'action'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: action
  topic: html
notes:
  - 'Needs updating, security considerations & clean up'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'Sets the URL which the browser will send the form data on submission.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/action

---
## Summary

Sets the URL which the browser will send the form data on submission.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
The action attribute is applied to a form element in order to instruct the browser of where to send the data upon submission. If it is not specified, the browser will automatically send data back to the current address.

### Best practices

It is recommended that you use an absolute URL for the action instead of a relative URL. Using an absolute URL means you know exactly where the form is going all the time, a relative URL may cause it to go to other places if you are not careful.

### Mailto actions

It is possible to make an email form by placing an mailto address in the action attribute. Although it is technically possible, we recommend strongly to 'not' use them, as it doesn't work in every browser as it was once supposed to. Please use an email script instead, and make the form post to that certain email script.

## Examples

This example uses the **action** attribute to post a form to a specified URL.

``` html
<!doctype html>
<title>Contact Form Demonstration</title>

<form action="http://example.com/contact" method="post">
    <label for="email">Email: </label>
    <input id="email" name="email" type="email" required>

    <label for="name">Name:</label>
    <input id="name" name="name" required>

    <label for="message">Message: </label>
    <textarea id="message" name="message">
    </textarea>

    <button>Submit</button>
</form>
```

## Notes

### Remarks

Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **action** attribute depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **action** returns an absolute URL. The value specified by the page author is returned when **action** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8. The value of the **action** attribute depends on the context of the reference to the attribute. When read as a DOM attribute, **action** returns an absolute URL. The value specified by the page author is returned when **action** is read as a content attribute.

## Related specifications

[HTML5](http://www.w3.org/TR/html5/forms.html#attr-fs-action)
:   Candidate Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   **action**

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

-   [HTML Form Element](/html/elements/form)
