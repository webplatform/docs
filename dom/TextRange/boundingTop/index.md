---
title: boundingTop
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Retrieves the distance between the top edge of the rectangle that bounds the TextRange object and the top side of the object that contains the TextRange. '
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm'
uri: dom/TextRange/boundingTop

---
# boundingTop

## Summary

Retrieves the distance between the top edge of the rectangle that bounds the TextRange object and the top side of the object that contains the TextRange.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/TextRange](/dom/TextRange)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = textRange.boundingTop;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

the top coordinate of the bounding rectangle, in pixels.

## Examples

This example retrieves the value of the **boundingTop** property for the given text area.

``` {.html}
<script type="text/javascript">
function boundDim(oObject)
{
    var oTextRange = oObject.createTextRange();
    if (oTextRange != null) {
        alert("The bounding top is \n" +
            oTextRange.boundingTop + oObject.scrollTop);
    }
}
</script>
</head>
<body>
<textarea cols="100" rows="2" id="oTextarea"
    onclick="boundDim(this)"> . . . </textarea>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm)

## Notes

### Remarks

**Note**  If the [**TextRange**](/dom/TextRange) is inside a **textArea** object, add the value of the element's [**scrollTop**](/dom/HTMLElement/scrollTop) property to the value of **boundingTop**.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[boundingTop Property](http://msdn.microsoft.com/en-us/library/ie/ms533540(v=vs.85).aspx) Article]

