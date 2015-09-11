---
title: name
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/Dyn_Name_Sample.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/createElement
    - dom/attributes
uri: html/attributes/name

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

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
## <span>Examples</span>

The following example shows how to set the **NAME** attribute on a dynamically created [**A**](/html/elements/a) element.

``` html
var oAnchor = document.createElement("<A NAME='AnchorName'></A>");
```

The following example shows how to set the **NAME** attribute on a dynamically created [**A**](/html/elements/a) element. This example assumes that ppvDocument is a valid **IHTMLDocument2** interface pointer, and ppvElement is a valid **IHTMLElement** interface pointer.

``` html
ppvDocument->createElement(CComBSTR("<A NAME='AnchorName'></A>"), &ppvElement)
```

The following example shows how to set the **NAME** dynamically on objects (option buttons) created with the [**createElement**](/w/index.php?title=dom/methods/createElement&action=edit&redlink=1) method.

``` html
var inp = document.createElement('input');
    inp.setAttribute('type',  'radio');
    inp.setAttribute('name',  'Q'+count);
    inp.setAttribute('value', answers[i]);
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/Dyn_Name_Sample.htm)

## <span>Notes</span>

### <span>Remarks</span>

When you submit a **form**, use the **name** property to bind the value of the control. The name is not the value that is displayed for the **input type=button**, **input type=reset**, and **input type=submit** input types. The internally stored value is submitted with the form, not the displayed value. When you submit a **form**, use the **name** property to bind the value of the control. The name is not the value displayed for the **input type=button**, **input type=reset**, and **input type=submit** input types. The internally stored value is submitted with the **form**, not the displayed value. Microsoft JScript allows you to change the name at run time. This does not cause the name in the programming model to change in the collection of elements, but it does change the name that you use for submitting elements. Windows Internet Explorer 8 and later. In IE8 Standards mode, dynamically setting the **name** attribute on an **input type=radio** button correctly applies that button to the same named group. For more information about IE8 mode, see Defining Document Compatibility. In Internet Explorer 8 and later versions, you can set the **NAME** attribute at run time on elements that are dynamically created with the [**createElement**](/w/index.php?title=dom/methods/createElement&action=edit&redlink=1) method. To create an element with a **NAME** attribute in earlier versions of Windows Internet Explorer, include the attribute and its value when you use the **createElement** method. In Microsoft Internet Explorer 6 and later versions, this property applies to the [**attribute**](/w/index.php?title=dom/attributes&action=edit&redlink=1) object.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.3

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `a`
-   `applet`
-   `attribute`
-   `button`
-   `embed`
-   `form`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
-   `input type=hidden`
-   `input type=image`
-   `input type=password`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=text`
-   `link`
-   `map`
-   `object`
-   `rt`
-   `ruby`
-   `select`
-   `textArea`
