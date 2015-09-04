---
title: createProcessingInstruction
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Creates a processing instruction for an XML parser.'
uri: dom/Document/createProcessingInstruction

---
# createProcessingInstruction

## Summary

Creates a processing instruction for an XML parser.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var processingInstruction = document.createProcessingInstruction(target, data);
```

## Parameters

### target

 Data-typeÂ
:   String

 The name of the processing instruction.

### data

 Data-typeÂ
:   String

 The data for the processing instruction.

## Return Value

Returns an object of type DOM Node.

The created processing instruction.

## Examples

The following code example demonstrates how to create an XML processing instruction.

``` {.js}
// This example creates the following processing instruction:
//   <?xml-stylesheet type="text/css" href="style.css">
var sTarget = 'xml-stylesheet';
var sData = 'type="text/css" href="style.css"';'
var obj = document.createProcessingInstruction(sTarget, sData);
```

## Notes

The **createProcessingInstruction** method is supported only for XML documents.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-135944439)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

