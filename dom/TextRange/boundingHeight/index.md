---
title: 'boundingHeight'
attributions:
  - 'Microsoft Developer Network: [[boundingHeight Property](http://msdn.microsoft.com/en-us/library/ie/ms533538(v=vs.85).aspx) Article]'
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
summary: 'Retrieves the height of the rectangle that bounds the TextRange object.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/TextRange/boundingHeight

---
## Summary

Retrieves the height of the rectangle that bounds the TextRange object.

Property of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.boundingHeight;
```

## Return Value

Returns an object of type NumberNumber

the height of the bounding rectangle, in pixels.

## Examples

This example retrieves the value of the **boundingHeight** property for the given text area.

``` js
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
