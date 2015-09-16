---
title: removeExpression
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeExpression.htm'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/cssom/methods
    href: /css/cssom/methods
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /css/cssom/methods
tags:
  - API
  - Object
  - Methods
  - DOM
uri: css/cssom/methods/removeExpression

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [css/cssom/methods](/css/cssom/methods)[css/cssom/methods](/css/cssom/methods)

## Syntax

``` js
var object = object.removeExpression(PropertyName);
```

## Parameters

### PropertyName

 Data-type
:   String

**String** that specifies the name of the property from which to remove an expression.

## Return Value

Returns an object of type BooleanBoolean

Returns **true** if the expression was successfully removed, **false** otherwise.

## Examples

This example uses the **removeExpression** method to remove an expression from the [**width**](/css/properties/width) property of a blue box.

``` html
<INPUT TYPE=text ID=oBox1 value=40>The sum of the values in these two text boxes determines the width <BR><INPUT TYPE=text ID=oBox2 value=40>of the blue text box below.
<BR><INPUT TYPE=text ID=oBox3 STYLE="background-color:blue">
<BR><BR><INPUT TYPE=button ID=Button1
    value="Step 1: Get expression" onclick="getexp()">
<INPUT TYPE=button ID=Button2 value="Step 2: Remove expression"
    onclick="remexp()">
<INPUT TYPE=button ID=Button3 value="Step 3: Get expression again"
    onclick="getexp()">
<BR>
<HR>
<BR>
Right-click anywhere on this page to view the source code.

<SCRIPT>
var s;
var b;
oBox3.style.setExpression("width","eval(oBox1.value) +
    eval(oBox2.value)","jscript");
function getexp()
{
    s=oBox3.style.getExpression("width");
    alert("Expression for the width of the blue box is \n\n" + s +
    "\n\nThe width property has a value of " + oBox3.style.width);
}
function remexp()
{
    b = oBox3.style.removeExpression("width");
    alert("Expression removed successfully? \n" + b);
}
</SCRIPT>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeExpression.htm)

## Notes

### Remarks

After the expression is removed from the specified property, the value of the property equals the last computed value of the expression. To remove expressions set by the [**setExpression**](/css/cssom/methods/setExpression) method, use **removeExpression**. The following syntax sections show how to remove an expression from supported Cascading Style Sheets (CSS) attributes and DHTML Properties.

-   Use this syntax to remove an expression from a read/write property or from an **expando** property.

`object.removeExpression(sPropertyName)`

-   Use this syntax to remove an expression from a CSS attribute.

`object.style.removeExpression(sPropertyName)`

## See also

### Related pages (MSDN)

-   `IHTMLElement2`
-   `IHTMLStyle2`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `getExpression`
-   `Conceptual`
-   `About Dynamic Properties`
