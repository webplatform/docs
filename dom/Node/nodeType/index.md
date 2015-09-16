---
title: 'nodeType'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.nodeType](https://developer.mozilla.org/en-US/docs/Web/API/Node.nodeType) Article]'
  - 'Microsoft Developer Network: [[nodeType Property](http://msdn.microsoft.com/en-us/library/ie/ms534191(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the type of the requested node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/nodeType

---
## Summary

Retrieves the type of the requested node.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## Syntax

**Note**: This property is read-only.

``` js
var nodeType = node.nodeType;
```

## Return Value

Returns an object of type NumberNumber

One of the node type constants defined on [Node](/dom/Node), or null.

Node.ELEMENT\_NODE =1

Node.ATTRIBUTE\_NODE = 2

Node.TEXT\_NODE = 3

Node.CDATA\_SECTION\_NODE = 4

Node.ENTITY\_REFERENCE\_NODE = 5

Node.ENTITY\_NODE = 6

Node.PROCESSING\_INSTRUCTION\_NODE = 7

Node.COMMENT\_NODE = 8

Node.DOCUMENT\_NODE = 9

Node.DOCUMENT\_TYPE\_NODE = 10

Node.DOCUMENT\_FRAGMENT\_NODE = 11

Node.NOTATION\_NODE = 12

## Examples

This example assigns the **nodeType** property of the **body** object to a variable.

``` js
var iType = document.body.nodeType;
```

This example assigns the **nodeType** property of a node created with the [**createElement**](/dom/Document/createElement) method to a variable.

``` js
var oNode = document.createElement("B");
document.body.insertBefore(oNode);
var iType = oNode.nodeType;
```

This example users the node constants to return the nodeType description.

``` js
function getNodeTypeName(nType){
   switch (nType){
        case Node.ELEMENT_NODE:
            return 'ELEMENT_NODE';
        case Node.ATTRIBUTE_NODE:
            return 'ATTRIBUTE_NODE';
        case Node.TEXT_NODE:
            return 'TEXT_NODE';
        case Node.CDATA_SECTION_NODE:
            return 'CDATA_SECTION_NODE';
        case Node.ENTITY_REFERENCE_NODE:
            return 'ENTITY_REFERENCE_NODE';
        case Node.ENTITY_NODE:
            return 'ENTITY_NODE';
        case Node.PROCESSING_INSTRUCTION_NODE:
            return 'PROCESSING_INSTRUCTION_NODE';
        case Node.COMMENT_NODE:
            return 'COMMENT_NODE';
        case Node.DOCUMENT_NODE:
            return 'DOCUMENT_NODE';
        case Node.DOCUMENT_TYPE_NODE:
            return 'DOCUMENT_TYPE_NODE';
        case Node.DOCUMENT_FRAGMENT_NODE:
            return 'DOCUMENT_FRAGMENT_NODE';
        case Node.NOTATION_NODE:
            return 'NOTATION_NODE';
        default:
            return 'unknown nodeType:'+ntype;
      }
   }
```

## Notes

If the node represents an attribute retrieved from the [**attributes**](/dom/Node/attributes) collection, the **nodeType** returns `null`.

The proprietary \<comment\> element is recognized as a HTMLUnknown element in IE10 and higher and returns ELEMENT\_NODE as its type.

Use the HTML comment block instead.

\<-- this is a hidden comment tag --\>

\<comment\> this is a legacy IE comment tag and will display on your web page... do not use or remove from your legacy pages\</comment\>

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
