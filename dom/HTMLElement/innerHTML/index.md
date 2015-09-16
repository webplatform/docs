---
title: 'innerHTML'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerHTML.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertScript_2.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerHTMLsafe.htm'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/innerHTML

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.innerHTML;
element.innerHTML = value;
```

## Examples

This example uses the **innerHTML** property to change the text of a paragraph when an [**onmouseover**](/dom/MouseEvent/mouseover) event occurs. The affected text and any tags within it are changed by the **onmouseover** and [**onmouseout**](/dom/MouseEvent/mouseout) events.

``` html
...
<P onmouseover="this.innerHTML='<B>Mouse out to change back.</B>'"
    onmouseout="this.innerHTML='<I>Mouse over again to change.</I>'">
    <I>Mouse over this text to change it.</I>
</P>
...
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerHTML.htm)

This example uses the **innerHTML** property to insert script into the page.

``` html
<HTML>
<SCRIPT>
function insertScript(){
    var sHTML="<input type=button onclick=" + "go2()" + " value='Click Me'><BR>";
    var sScript="<SCRIPT DEFER>";
    sScript = sScript + "function go2(){ alert('Hello from inserted script.') }";
    sScript = sScript + "</SCRIPT" + ">";
    ScriptDiv.innerHTML = sHTML + sScript;
}
</SCRIPT>
<BODY onload="insertScript();">
    <DIV ID="ScriptDiv"></DIV>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertScript_2.htm)

The following example demonstrates how to convert the HTML source to text using a temporary **div** element and [**createTextNode**](/dom/Document/createTextNode). Once the HTML is sanitized, it can be safely inserted into the document using **innerHTML**.

``` html
<body onload="displaySource()">

<script type="text/javascript">
function sanitizeHTML(s) {
    var d = document.createElement('div');
    d.appendChild(document.createTextNode(s));
    return d.innerHTML;
}

function displaySource()
{
    var h = sanitizeHTML(document.documentElement.outerHTML);
    document.getElementById('asHTML').innerHTML = "<pre>" + h + "</pre>";
    document.getElementById('asText').innerText = h;
}
</script>

<h2>As HTML</h2>
<div id="asHTML"></div>
<h2>As Text</h2>
<div id="asText"></div>

</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerHTMLsafe.htm)

## Notes

### Remarks

The **innerHTML** property is valid for both block and inline elements. By definition, elements that do not have both an opening and closing tag cannot have an **innerHTML** property. The **innerHTML** property takes a string that specifies a valid combination of text and elements. When the **innerHTML** property is set, the given string completely replaces the existing content of the object. If the string contains HTML tags, the string is parsed and formatted as it is placed into the document. This property is accessible at run time as the document is being parsed; however, removing elements at run time, before the document is fully loaded, could prevent other areas of the document from rendering. When using **innerHTML** to insert script, you must include the [**DEFER**](/html/attributes/defer) attribute in the **script** element. The **innerHTML** property is read-only on the **col**, **colGroup**, **frameSet**, **html**, **head**, **style**, [**table**](/html/elements/table), **tBody**, **tFoot**, **tHead**, **title**, and **tr** objects. You can change the value of the **title** element using the [**Document**](/dom/Document).title property. To change the contents of the [**table**](/html/elements/table), **tFoot**, **tHead**, and **tr** elements, use the table object model described in Building Tables Dynamically. However, to change the content of a particular cell, you can use **innerHTML**.

**Security Warning:  ** Improper handling of the **innerHTML** property can enable script-injection attacks. When accepting text from an untrusted source (such as the query string of a URL), use [**createTextNode**](/dom/Document/createTextNode) to convert the HTML to text, and append the element to the document using [**appendChild**](/dom/Node/appendChild). Refer to the Examples section below for more information. To maintain compatibility with earlier versions of Windows Internet Explorer, this property applies to the **textArea** object. However, the property works only with strings that do not contain tags. With a string that contains a tag, this property returns an error. It is better to use the [**innerText**](/dom/HTMLElement/innerText) property with this object.

### Syntax
