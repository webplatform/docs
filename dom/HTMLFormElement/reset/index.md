---
title: 'reset'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/reset.htm'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLFormElement
    href: /dom/HTMLFormElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLFormElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLFormElement/reset

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLFormElement](/dom/HTMLFormElement)[dom/HTMLFormElement](/dom/HTMLFormElement)

## Syntax

``` js
var object = object.reset();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example demonstrates how to use the **reset** method for a **form** object. When the button is pressed, the **form** is reset, resulting in the [**onreset**](/dom/Element/reset) event call on the **form** object. The **onreset** event calls an event handler which in turn adds the text `Resetting form.` to the text area below.

``` html
<HTML>
<HEAD>
<SCRIPT>
function doReset(){
    oTextArea1.value += "Resetting form.  ";
}
</SCRIPT>
</HEAD>
<BODY>
<DIV id="oDiv1"
    style="border:1px solid black; background:#EEEEEE; padding:10px;">
    <B>Form</B>
    <FORM name="form1" onreset="doReset();">
        <b>Enter some text:</b> <INPUT type="text" name="oText1" value=""><BR><BR>
        <BUTTON onclick="form.reset();">form.reset()</BUTTON>
    </FORM>
</DIV>
<B>Text area</B><BR>
<TEXTAREA id="oTextArea1" value="" rows="5" cols="75"></TEXTAREA>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/reset.htm)

## Notes

### Remarks

The **reset** method raises the **onreset** event on the form. The **reset** method fires the [**onreset**](/dom/Element/reset) event on the form.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages

-   `form`
