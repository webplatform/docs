---
title: 'focus'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onfocusEX.htm'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
tags:
  - Events
  - DOM
uri: dom/FocusEvent/focus

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

This example uses the **onfocus** event to make **INPUT\_text** and **label** objects more accessible. When the **INPUT\_text** object has focus, the **onfocus** event fires and the [**backgroundColor**](/css/properties/background-color), [**fontSize**](/css/properties/font-size), and [**fontWeight**](/css/properties/font-weight) properties are changed to give the control more prominence.

``` js
...
<style type="text/css">
.normal {
    background-color: white;
    color: black;
    font-weight: normal;
    font-size: 8pt;
    font-family: Arial;
}
.accessible {
    background-color: silver;
    font-weight: bold;
    font-size: 10pt;
}
</style>
<script type="text/javascript">
function fnSetStyle(){
   event.srcElement.className="accessible";
   var oWorkLabel=eval(event.srcElement.id + "_label");
   oWorkLabel.className="accessible";
}
</script>
<label for="oInput" class="normal" id="oInput_label">Enter some text</label>
<input type="text" class="normal" onfocus="fnSetStyle()" id="oInput">
...
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onfocusEX.htm)

## Notes

### Remarks

**Note**  Using the [**setActive**](/dom/HTMLElement/setActive) method has no effect on document focus. Using the ****focus**** method on an individual element causes the element to gain focus and become the active element. When one object loses activation and another object becomes the [**activeElement**](/dom/Document/activeElement), the **onfocus** event fires on the object becoming the **activeElement** only after the [**onblur**](/dom/FocusEvent/blur) event fires on the object losing activation. Use the focus events to determine when to prepare an object to receive input from the user. Elements cannot receive focus until the document is finished loading. For Microsoft Internet Explorer 5.5 and later, focus on a [Document](/dom/Document), and the **active element** of a **document** can be managed separately. The synchronous events **onactivate** and **ondeactivate** provide better control for managing activation changes. As of Microsoft Internet Explorer 5, browser elements retain focus within the current history when the user returns to a page. To avoid firing the **onfocus** event unintentionally for an element when the document loads, invoke the **focus** method on another element. As of Internet Explorer 5, you can force elements that do not implicitly receive focus to receive focus by adding them to the document tabbing order using the [**TABINDEX**](/html/attributes/tabIndex) attribute. Sets focus to an object. To invoke this event, do one of the following:

-   Click an object.
-   Use keyboard navigation.
-   Invoke the ****focus**** method.
-   Invoke the [**setActive**](/dom/HTMLElement/setActive) method.

The *pEvtObj* parameter is required for the following interfaces:

-   **HTMLAnchorEvents2**
-   **HTMLAreaEvents2**
-   **HTMLButtonElementEvents2**
-   **HTMLControlElementEvents2**
-   **HTMLDocumentEvents2**
-   **HTMLElementEvents2**
-   **HTMLFormElementEvents2**
-   **HTMLImgEvents2**
-   **HTMLFrameSiteEvents2**
-   **HTMLInputFileElementEvents2**
-   **HTMLInputImageEvents2**
-   **HTMLInputTextElementEvents2**
-   **HTMLLabelEvents2**
-   **HTMLLinkElementEvents2**
-   **HTMLMapEvents2**
-   **HTMLMarqueeElementEvents2**
-   **HTMLObjectElementEvents2**
-   **HTMLOptionButtonElementEvents2**
-   **HTMLScriptEvents2**
-   **HTMLSelectElementEvents2**
-   **HTMLStyleElementEvents2**
-   **HTMLTableEvents2**
-   **HTMLTextContainerEvents2**
-   **HTMLWindowEvents2**
-   **HTMLDocumentEvents4**

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****
