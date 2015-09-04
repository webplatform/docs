---
title: hasAttributes
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
notes:
  - "Incorrect MSDN link removed.\nMSDN has no document for hasAttributes"
summary: 'Returns whether this node (if it is an element) has any attributes'
uri: dom/Node/hasAttributes

---
# hasAttributes

## Summary

Returns whether this node (if it is an element) has any attributes

*Method of [dom/Node](/dom/Node)*

## Syntax

``` {.js}
var bResult = object.hasAttributes();
```

## Return Value

Returns an object of type Boolean.

true if this node has any attributes, false otherwise.

## Examples

The following example will display an alert message that "the root element has attributes'. No following alert is displayed for the body element as it has no attributes.

    <!DOCTYPE html>
    <html id="root" class="desktop">

    <head>
    <meta content="text/html; charset=utf-8" http-equiv="Content-Type">
    <title>hasAttributesExample</title>
    </head>

    <body>
    <script type="text/javascript">
    var re=document.getElementById('root');
    if(re.hasAttributes()){alert('the root element has attributes');}
    var be=document.body;
    if(be.hasAttributes()){alert('the body element has attributes');}
    </script>
    </body>

    </html>

## Notes

### Remarks

The **hasAttributes** method determines whether the object has any attributes at all. The [**hasAttribute**](/dom/Element/hasAttribute) method tests for the existence of a specified attribute.

## Related specifications

Specification
:   Status
[DOM Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/core.html)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.hasAttributes](https://developer.mozilla.org/en-US/docs/Web/API/Node.hasAttributes) Article]

