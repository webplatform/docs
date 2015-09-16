---
title: NamedNodeMap
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[NamedNodeMap](https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'A collection of nodes that can be accessed by name. Objects contained in a NamedNodeMap may also be accessed by an ordinal index, but this is simply to allow convenient enumeration of the contents of a NamedNodeMap, and does not imply that the DOM specifies an order to these nodes.'
tags:
  - API
  - Objects
  - DOM
uri: dom/NamedNodeMap

---
## DOM Level 3

For technical reasons, the title of this article is not the text used to call this API. Instead, use `DOM Level 3`

## Summary

A collection of nodes that can be accessed by name. Objects contained in a NamedNodeMap may also be accessed by an ordinal index, but this is simply to allow convenient enumeration of the contents of a NamedNodeMap, and does not imply that the DOM specifies an order to these nodes.

## Properties

*No properties.*

## Methods

API Name
:   Summary

[getNamedItem](/dom/NamedNodeMap/getNamedItem)
:   Gets an attribute with a given name from an element.

[getNamedItemNS](/dom/NamedNodeMap/getNamedItemNS)
:   Gets an attribute with a given name and a given namespace.

[removeNamedItem](/dom/NamedNodeMap/removeNamedItem)
:   Removes an attribute with a given name.

[removeNamedItemNS](/dom/NamedNodeMap/removeNamedItemNS)
:   Removes an attribute with a given name and a given namespace.

[setNamedItem](/dom/NamedNodeMap/setNamedItem)
:   Adds an attribute to an element by using an attributes collection.

[setNamedItemNS](/dom/NamedNodeMap/setNamedItemNS)
:   Sets an attribute object as part of the object.

## Events

*No events.*

## Examples

This example uses the **attribute** object to create a list of attributes that are [**specified**](/dom/HTMLElement/specified).

``` html
<script type="text/javascript">
function fnFind(){
   for(var i=0;i<oList.attributes.length;i++){
      if(oList.attributes[i].specified){
         alert(oList.attributes[i].nodeName + ' = '
          + oList.attributes[i].nodeValue);
      }
   }
}
</script>
<ul onclick="fnFind()">
<li id = "oList" accesskey= "L">List Item 1</li>
</ul>
```

## Notes

### Remarks

The **attribute** object is accessible through the [**attributes**](/dom/Node/attributes) collection. A valid attribute or property can be any Dynamic HTML (DHTML) property or event that applies to the object. When displaying a Web page in IE8 Standards mode, Windows Internet Explorer distinguishes between attribute values specified by the original page author and the representation of those values in the DOM. For more information, see Attribute Differences in Internet Explorer 8. This object is available in script as of Microsoft Internet Explorer 5.
