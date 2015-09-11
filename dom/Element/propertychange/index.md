---
title: propertychange
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onpropertychangeEX.htm'
notes:
  - 'Needs summary,  spec, and compat'
readiness: 'In Progress'
tags:
  - Events
uri: dom/Element/propertychange

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

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
## <span>Examples</span>

This example demonstrates how to use the **onpropertychange** event to determine the name and value of an updated property.

``` html
<html>
<head>
<script type="text/javascript">
function changeProp()
{
    oProp.value = sText.value;
}
function changeCSSProp()
{
    if(oSelect.selectedIndex==0) oStyleProp.style.color= "white";
    else oStyleProp.style.color = "black";
    oStyleProp.style.backgroundColor = oSelect.value;
}
function Results(){
    sSrc.innerText = event.srcElement.id;
    sProperty.innerText = event.propertyName;
}
</script>
</head>
<body>
<div style="background: #eeeeee; padding: 10px;">
    Click the button below to change its 'Value' property to the string specified
    in the text box.<br><br>
  <input type="text" style="width: 250px" id="sText" value="Enter Some Text">
    &nbsp;
  <input type="button" id="oProp" onclick="changeProp()" value="Change property" onpropertychange="Results();">
  <p>Click the button below to change its 'backgroundColor' Cascading Style Sheet
    (CSS) property to the color specified in the drop-down list box.<br>
  <select name="oSelect" style="width: 150px">
        <option value="black" style="color: black">Black</option>
        <option value="blue" style="color: blue">Blue</option>
        <option value="green" style="color: green">Green</option>
        <option value="red" style="color: red">Red</option>
  </select>&nbsp;
  <input type="button" id="oStyleProp" onclick="changeCSSProp()" value="Change property" onpropertychange="Results();"></p>
  <br><br>
  <div style="border: 1px solid #cccccc; width: 100%; padding: 10px; background: white;">
    <b>Source object:</b> <span id="sSrc" style="color: red;"></span><br>
    <b>Property Name:</b> <span id="sProperty" style="color: red;"></span>
  </div>
</div>
<br>
<br>
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onpropertychangeEX.htm)

## <span>Notes</span>

### <span>Remarks</span>

The **onpropertychange** event fires when properties of an object, expando, or style sub-object change. To retrieve the name of the changed property, use the **TransitionEvent** object's [**propertyName**](/dom/TransitionEvent/propertyName) property. This property returns a read-only string of the name of the property that has changed. In the case of Cascading Style Sheets (CSS) properties, the property name is prefixed with `style`. For example, if the CSS property [**pixelLeft**](/css/cssom/properties/pixelLeft) is altered, the value of `window.event.propertyName` is **style.left**. By contrast, if the non-CSS property [**name**](/html/attributes/name_(frames)) is altered, the value of `window.event.propertyName` is **name**. When the **onpropertychange** event fires, the **srcElement** property of the **event** object is set to the object whose property has changed. **Note**  Changing the [**innerText**](/dom/HTMLElement/innerText) or [**innerHTML**](/dom/HTMLElement/innerHTML) of child elements will not cause the **onpropertychange** event to fire for the parent element. Sends notification when a property changes. To invoke this event, do one of the following:

-   Cause a property to change value.

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

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

