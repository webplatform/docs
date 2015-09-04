---
title: boundingLeft
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Retrieves the distance between the left edge of the rectangle that bounds the TextRange object and the left side of the object that contains the TextRange.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm'
uri: dom/TextRange/boundingLeft

---
# boundingLeft

## Summary

Retrieves the distance between the left edge of the rectangle that bounds the TextRange object and the left side of the object that contains the TextRange.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/TextRange](/dom/TextRange)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = textRange.boundingLeft;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

the left coordinate of the bounding rectangle, in pixels.

## Examples

This example retrieves the value of the **boundingLeft** property for the given text area.

``` {.js}
<script type="text/javascript">
function boundDim(oObject)
{
    var oTextRange = oObject.createTextRange();
    if (oTextRange != null) {
        alert("The bounding left is \n" +
            oTextRange.boundingLeft);
    }
}
</script>
</head>
<body>
<textarea cols="100" rows="2" id="oTextarea"
    onclick="boundDim(this)"> . . . </textarea>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm)

### Syntax

result = textRange.boundingLeft;

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[boundingLeft Property](http://msdn.microsoft.com/en-us/library/ie/ms533539(v=vs.85).aspx) Article]

