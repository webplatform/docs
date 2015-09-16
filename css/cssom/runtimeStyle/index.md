---
title: 'runtimeStyle'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/runtimeStyle.htm'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
summary: 'Sets and retrieves the format and style of an object.'
tags:
  - API
  - Objects
  - DOM
uri: css/cssom/runtimeStyle

---
## Summary

Sets and retrieves the format and style of an object.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Examples

This example sets a value on the **runtimeStyle** object to affect the [**currentStyle**](/css/cssom/currentStyle) object, but not the [**style**](/css/cssom/style) object.

``` js
<SCRIPT>
function fnChangeValue(sValue){
   if(oDIV.runtimeStyle.backgroundColor == oDIV.style.backgroundColor){
      sValue="";
   }
   oDIV.runtimeStyle.backgroundColor = sValue;
   console.log(oDIV.style.backgroundColor +
      "\n" + oDIV.currentStyle.backgroundColor +
      "\n" + oDIV.runtimeStyle.backgroundColor);
}
</SCRIPT>
<DIV ID = "oDIV">
This is a demonstration DIV.
</DIV>
<INPUT TYPE = "button" VALUE = "Change Color" onclick="fnChangeValue('blue')">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/runtimeStyle.htm)

## Notes

### Remarks

The **runtimeStyle** object sets and retrieves the format and style of an object, and overrides existing formats and styles in the process. Other than having precedence over the [**style**](/css/cssom/style) object and not persisting, the **runtimeStyle** object is equivalent to the **style** object. To change or clear multiple style properties simultaneously, use this object with the [**cssText**](/css/cssom/styleSheet/cssText) property. For example, to change the font color and background color of a **DIV** element, you could use the following code:

    <DIV onclick="this.runtimeStyle.cssText = 'color:red;background-color:blue;border:5px solid black;'">
    Click this DIV to change style properties.</DIV>

Windows Internet Explorer 8 or later. The behavior of [**setAttribute**](/dom/Element/setAttribute) method depends on the current document compatibility mode. For more information, see Attribute Differences in Internet Explorer 8.

## See also

### Related pages

-   currentStyle[currentStyle](/css/cssom/currentStyle)
