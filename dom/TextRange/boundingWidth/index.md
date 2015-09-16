---
title: 'boundingWidth'
attributions:
  - 'Microsoft Developer Network: [[boundingWidth Property](http://msdn.microsoft.com/en-us/library/ie/ms533541(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/TextRange
    href: /dom/TextRange
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/TextRange
standardization_status: Non-Standard
summary: 'Retrieves the width of the rectangle that bounds the TextRange object'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/TextRange/boundingWidth

---
## Summary

Retrieves the width of the rectangle that bounds the TextRange object

Property of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

**Note**: This property is read-only.

``` js
var result = textRange.boundingWidth;
```

## Return Value

Returns an object of type NumberNumber

the width of the bounding rectangle, in pixels.

## Examples

This example retrieves the value of the **boundingWidth** property for the given text area.

``` html
<script type="text/html">
function boundDim(oObject)
{
    var oTextRange = oObject.createTextRange();
    if (oTextRange != null) {
        alert("The bounding width is \n" +
            oTextRange.boundingWidth);
    }
}
</script>
</head>
<body>
<textarea cols="100" rows="2" id="oTextarea"
    onclick="boundDim(this)">  </textarea>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/boundingTop.htm)

### Syntax
