---
title: 'boundingLeft'
attributions:
  - 'Microsoft Developer Network: [[boundingLeft Property](http://msdn.microsoft.com/en-us/library/ie/ms533539(v=vs.85).aspx) Article]'
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
summary: 'Retrieves the distance between the left edge of the rectangle that bounds the TextRange object and the left side of the object that contains the TextRange.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/TextRange/boundingLeft

---
## Summary

Retrieves the distance between the left edge of the rectangle that bounds the TextRange object and the left side of the object that contains the TextRange.

Property of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

**Note**: This property is read-only.

``` js
var result = textRange.boundingLeft;
```

## Return Value

Returns an object of type NumberNumber

the left coordinate of the bounding rectangle, in pixels.

## Examples

This example retrieves the value of the **boundingLeft** property for the given text area.

``` js
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
