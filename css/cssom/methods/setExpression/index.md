---
title: setExpression
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec reference, standardization status'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/recalc_inline.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setExpression.htm'
uri: css/cssom/methods/setExpression

---
# setExpression

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [css/cssom/methods](/css/cssom/methods)*

## Syntax

``` {.js}
var object = object.setExpression(PropertyName, Expression, Language);
```

## Parameters

### PropertyName

 Data-typeÂ
:   String

**String**Â that specifies the name of the property to which *expression* is added.

### Expression

 Data-typeÂ
:   String

**String**Â that specifies any valid script (JScript, JavaScript, VBSCript) statement without quotations or semicolons. This string can include references to other properties on the current page. Array references are not allowed on object properties included in this script.

### Language

 Data-typeÂ
:   String

**String**Â that specifies one of the following values:

-   "JScript" -- Default. Language is JScript.
-   "VBScript" --Language is VBScript.
-   "JavaScript" -- Language is JavaScript.

## Return Value

Returns an object of type DOM Node.

## Examples

The following examples use the **setExpression** method to change the width of a blue box. In each example, the width of the blue box is equal to the sum of the values of the first two text boxes. When a value in one of the text boxes changes, the width of the blue box recalculates.

This example shows the HTML implementation of **setExpression**.

``` {.html}
<INPUT TYPE=text ID=oBox1 value=40>The sum of the values in
    these two text boxes determines the width<BR>
<INPUT TYPE=text ID=oBox2 value=40>of the blue text box below.
<BR><INPUT TYPE=text ID=oBox3
    STYLE="width:expression(eval(oBox1.value) +
    eval(oBox2.value));background-color:blue">
<BR><INPUT TYPE=button ID=Button
    value="Click to resize blue box above"
    onclick="recalc()">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/recalc_inline.htm)

This example uses the [**uniqueID**](/dom/HTMLElement/uniqueID) property and the **setExpression** method to update the [**innerText**](/dom/HTMLElement/innerText) property of a table row.

``` {.js}
<SCRIPT>
window.onload=fnInit;
function fnInit(){
   var iLen=oSheet.rows.length-1;
   for(var i=1;i<iLen;i++){
      var oRow=oSheet.rows[i];
      var oCells=oRow.cells;
      oCells(3).setExpression("innerText",
         "fnGetValue(" + oRow.uniqueID + ")");
   }
   var oGrand=oSheet.rows(iLen).cells(1);
   oGrand.setExpression("innerText","fnGetTotal()");
}
function fnGetTotal(){
   var iValue=0;
   var iLen=oSheet.rows.length-1;
   for(var i=1;i<iLen;i++){
      iValue+=parseFloat(oSheet.rows(i).cells(3).innerText);
   }
   return iValue;
}
function fnGetValue(oRow){
   var oCells=oRow.cells;
   var oPrice=oCells(2);
   var oQuantity=oCells(1);
   var sPrice;
   var sQuantity;
   if(oPrice.childNodes[0].nodeName=="#text"){
      sPrice=oPrice.innerText;
   }
   else{
      var vPrice=oPrice.childNodes[0].value;
      sPrice=(vPrice==""?"0":vPrice);
   }
   if(oQuantity.childNodes[0].nodeName=="#text"){
      sQuantity=oQuantity.innerText;
   }
   else{
      var vQuantity=oQuantity.childNodes[0].value;
      sQuantity=(vQuantity==""?"0":vQuantity);
   }
   var vAlg1=parseFloat(sPrice) * parseFloat(sQuantity);
   return vAlg1;
}
</SCRIPT>
<TABLE ID="oSheet">
<TR><TH>Product</TH><TH>Quantity</TH>
<TH>Price per #</TH><TH>Totals</TH></TR>
<TR><TD>Browser Putty</TD><TD EDIT="true">2</TD>
<TD EDIT="true">4.99</TD><TD></TD></TR>
<TR><TH COLSPAN=3>Grand Total</TH><TH></TH></TR>
</TABLE>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setExpression.htm)

## Notes

### Remarks

Use the **setExpression** method to add expressions to supported [**removeExpression**](/css/cssom/methods/removeExpression) method. The following syntax sections show how to set an expression on DHTML Properties and CSS attributes.

-   Use this syntax to set an expression on a read/write property or on an **expando** property.

\<div class{{=}}"codeSnippet"\> \<pre xml:space{{=}}"preserve"\>\<code\>object.setExpression(sPropertyName, sExpression, sLanguage)\</code\>\</pre\> \</div\>

-   Use this syntax to set an expression on a CSS attribute.

\<div class{{=}}"codeSnippet"\> \<pre xml:space{{=}}"preserve"\>\<code\>object.style.setExpression(sPropertyName, sExpression, sLanguage)\</code\>\</pre\> \</div\>

-   Use the **expression()** syntax to set an expression on a CSS attribute in HTML.

\<div class{{=}}"codeSnippet"\> \<pre xml:space{{=}}"preserve"\>\<code\>\<ELEMENT STYLE{{=}}"sAttributeName:expression(sExpression)"\>\</code\>\</pre\> \</div\> The data type of the evaluated expression in the *language* parameter must match one of the possible values allowed for the *expression* parameter. If the property or attribute specified by the first parameter requires a string, the data type of the second parameter must be a string. Otherwise, the second parameter is evaluated prior to invoking **setExpression**, causing the expression to be set to the result of the evaluation. Use the [**uniqueID**](/dom/HTMLElement/uniqueID) property of an object in an expression to refer back to the object. Using **uniqueID** is an alternative to specifying an [**id**](/html/attributes/id) for expressions that use an object reference. The [**cssText**](/css/cssom/styleSheet/cssText) property is a unique property that is not compatible with the dynamic properties implementation. Do not use **cssText** with any dynamic property methods. The following examples illustrate common problems encountered with the *expression* parameter in **setExpression**. The *expression* appears valid, but may not be.

-   The provided *expression* is invalid because document.style.fontSize is "npx" and will not add to 13

`object.style.setExpression("height","document.style.fontSize + 13"); `

-   The provided *expression* is invalid when document.body.style.fontSize is previously unspecified

`object.style.setExpression("width","document.body.style.fontSize"); `

## See also

### Related pages (MSDN)

-   `IHTMLElement2`
-   `IHTMLStyle2`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `getExpression`
-   `removeExpression`
-   `Conceptual`
-   `About Dynamic Properties`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

