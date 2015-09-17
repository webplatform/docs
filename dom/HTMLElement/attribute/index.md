---
title: 'attribute'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/attribute

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.attribute;
element.attribute = value;
```

## Examples

This example shows how to iterate through the collection of attributes of the specified object, displaying the name and value of the attributes as well as the language of the attribute (HTML or script).

``` js
<SCRIPT>
function ShowAttribs(oElem)
{
    txtAttribs.innerHTML = '';
    // Retrieve the collection of attributes for the specified object.
    var oAttribs = oElem.attributes;
    // Iterate through the collection.
    for (var i = 0; i < oAttribs.length; i++)
    {
        var oAttrib = oAttribs[i];
        // Print the name and value of the attribute.
        // Additionally print whether or not the attribute was specified
        // in HTML or script.
        txtAttribs.innerHTML += oAttrib.nodeName + '=' +
            oAttrib.nodeValue + ' (' + oAttrib.specified + ')<BR>';
    }
}
</SCRIPT>
```

## Notes

### Remarks

The **attributes** collection does not expose the [**style**](/css/cssom/style) object. Use the [**cssText**](/css/cssom/styleSheet/cssText) property of the object's **style** property to retrieve the persistent representation of the cascading styles associated with an object. Unlike other DHTML collections, such as [**children**](/dom/Element/children), the **attributes** collection is static. Modifications to the properties of an object are not automatically reflected by an existing reference to the **attributes** collection of that object.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.4

## See also

### Related pages

-   `About the W3C Document Object Model`
