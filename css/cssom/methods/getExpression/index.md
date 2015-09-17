---
title: 'getExpression'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getExpression.htm'
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
    value: 'DOM Node'
    href: /css/cssom/methods
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: css/cssom/methods/getExpression

---
Method of [css/cssom/methods](/css/cssom/methods)[css/cssom/methods](/css/cssom/methods)

## Syntax

``` js
var object = object.getExpression(PropertyName);
```

## Parameters

### PropertyName

 Data-type
:   String

**String** that specifies the name of the property from which to retrieve the expression.

## Return Value

Returns an object of type DOM NodeDOM Node

A variant value representing the expression of the property.

## Examples

The following examples demonstrate how to use the **getExpression** method to retrieve CSS properties. This example retrieves the [**width**](/css/properties/width) property of a **span** object.

``` html
<body>
<span id="trueBlueSpan"
    style="background-color:lightblue; width:100px">
    The width of this blue span is set inline at 100 pixels.
</span>
<span id="oldYellowSpan" style="background-color:lightyellow;
    width:200px">
    The width of this yelllow span is set inline at 200 pixels.
</span>
<br>
<span id="AlGreenSpan" style="background-color:lightgreen;
    width:expression(trueBlueSpan.style.pixelWidth +
    oldYellowSpan.style.pixelWidth)">
    Click the button below to see the expression used to set
    the width of this span.
</span>
<br>
<button onclick=alert(AlGreenSpan.style.getExpression("width"));>
    See Expression</button>
</body>
```

In the following example, the [**setExpression**](/css/cssom/methods/setExpression) method is used to set the [**width**](/css/properties/width) property of a blue **input type=text** object equal to the sum of the values in two other **input type=text** objects. When the user clicks the **input type=button** element, the **getExpression** method is used to display the expression.

``` html
<html>
<head>
<script language="JScript">
var s;
function fnInit() {
Box3.style.setExpression("width","eval(Box1.value) + eval(Box2.value)",
"jscript");
}
function getexp() {
s=Box3.style.getExpression("width");
alert("Expression for the width of the blue box is \n\n" + s +
"\n\nThe width property has a value of " + Box3.style.width);
}
</script>
</head>
<body onload=fnInit();>
<input type=text id="Box1" value=40>
<br><input type=text id="Box2" value=40>
<br><input type=text id="Box3" style="background-color:blue">
<br><input type=button id="Button2" value="Get expression" onclick="getexp()">
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getExpression.htm)

## Notes

### Remarks

The following syntax sections show how to retrieve an expression from supported Cascading Style Sheets (CSS) and DHTML Properties.

-   Use this syntax to retrieve an expression from a read/write property or from an **expando** property.

`var sExpression = object.getExpression(sPropertyName)`

-   Use this syntax to retrieve an expression from a CSS attribute.

`var sExpression = object.style.getExpression(sPropertyName)`

## See also

### Related pages

-   `IHTMLStyle2`
-   `IHTMLElement2`
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `Reference`
-   removeExpression[removeExpression](/css/cssom/methods/removeExpression)
-   setExpression[setExpression](/css/cssom/methods/setExpression)
-   `Conceptual`
-   `CSS Attributes: Index`
-   `About Dynamic Properties`
