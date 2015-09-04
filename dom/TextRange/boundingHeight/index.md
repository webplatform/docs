---
title: boundingHeight
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Retrieves the height of the rectangle that bounds the TextRange object.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm'
uri: dom/TextRange/boundingHeight

---
# boundingHeight

## Summary

Retrieves the height of the rectangle that bounds the TextRange object.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/TextRange](/dom/TextRange)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.boundingHeight;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

the height of the bounding rectangle, in pixels.

## Examples

This example retrieves the value of the **boundingHeight** property for the given text area.

``` {.js}
<script type="text/javascript">
function boundDim(oObject)
{
    var oTextRange = oObject.createTextRange();
    if (oTextRange != null) {
        alert("The bounding height is \n" +
            oTextRange.boundingHeight);
     }
}
</script>
</head>
<body>
<textarea cols="100" rows="2" id="oElmnt1"
    onclick="boundDim(this)"> . . . </textarea>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm)

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[boundingHeight Property](http://msdn.microsoft.com/en-us/library/ie/ms533538(v=vs.85).aspx) Article]

