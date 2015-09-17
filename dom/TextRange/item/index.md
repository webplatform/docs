---
title: 'item'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Looks like the generic Object.item() property..\nno listing on MSDN.\n\nNot a child of TextRange!"
readiness: 'Out of Date'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextRange
    href: /dom/TextRange
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/TextRange
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: dom/TextRange/item

---
Method of [dom/TextRange](/dom/TextRange)[dom/TextRange](/dom/TextRange)

## Syntax

``` js
var object = object.item(/* see parameter list */);
```

## Parameters

### pvarIndex

 Data-type
:   VARIANT

**Variant** of type **Integer** or **String** that specifies the object or collection to retrieve. If this parameter is an integer, it is the zero-based index of the object. If this parameter is a string, all objects with matching [**name**](/html/attributes/name) or [**id**](/html/attributes/id) properties are retrieved, and a collection is returned if more than one match is made.

## Return Value

Returns an object of type DOM NodeDOM Node

Variant

## Examples

The following example uses the **item** method to retrieve each object from the document. In this case, the method parameter is a number, so the objects are retrieved in the order in which they appear in the document.

``` html
<script language="JScript">
var oItem = document.all;
if (oItem!=null) {
    for (i=0; i<oItem.length; i++)
        alert(oItem.item(i).tagName);
}
</script>
```

The next example uses the **item** method to retrieve a collection of all objects in the document that have "Sample" as an **ID**. It then uses **item** again to retrieve each object from the "Sample" collection.

``` html
<script language="JScript">
var oItem = document.all.item("Sample");
If (oItem != null) {
    for (i=0; i<oItem.length; i++) {
        alert(oItem.item(i).tagName);
    }
}
</script>
```

## Notes

### Remarks

Always check the IDispatch pointer returned by this call, even if the method returns S\_OK. If the value of the pointer is null, the element was not found and the call was not successful. Upon successful return, the *pvarResult* parameter contains an IDispatch interface pointer or an array of IDispatch interface pointers that can be queried for a specific interface, depending on the collection type. **item** returns a **Variant** of type **Object** that can be queried for **IHTMLTxtRange**. Microsoft Internet Explorer 5 does not provide multiple selection. The default implementation of this method returns a collection consisting of a single **TextRange** object Host applications can provide a multiple selection mechanism and can return a collection of **TextRange** objects that represents discontinuous selections.
