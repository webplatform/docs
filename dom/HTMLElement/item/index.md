---
title: item
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'needs summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLElement/item

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var object = object.item(name, index);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   VARIANT

**Variant** of type **Integer** or **String** that specifies the object or collection to retrieve. If this parameter is an integer, it is the zero-based index of the object. If this parameter is a string, all objects with matching [**name**](/html/attributes/name) or [**id**](/html/attributes/id) properties are retrieved, and a collection is returned if more than one match is made.

### <span>index</span>

 Data-type
:   VARIANT

**Variant** of type **Integer** that specifies the zero-based index of the object to retrieve when a collection is returned.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Object

## <span>Examples</span>

The following example uses the **item** method to retrieve each object from the document. In this case, the method parameter is a number, so the objects are retrieved in the order they appear in the document.

``` html
<script language="JScript">
var coll = document.all;
if (coll!=null) {
    for (i=0; i<coll.length; i++)
        console.log(coll.item(i).tagName);
}
</script>
```

The next example uses the **item** method to retrieve a collection of all objects in the document that have "Sample" as an [**ID**](/html/attributes/id). The example then uses **item** again to retrieve each object from the "Sample" collection.

``` html
<script language="JScript">
var coll = document.all.item("Sample");
If (coll != null) {
    for (i=0; i<coll.length; i++) {
        console.log(coll.item(i).tagName);
    }
}
</script>
```

The last example is similar to the previous example, but uses the optional *index* parameter of **item** to retrieve individual objects.

``` html
<script language="JScript">
var coll = document.all.item("Sample")
if (coll!=null) {
    for (i=0; i<coll.length; i++)
        console.log(document.all.item("Sample",i).tagName);
}
</script>
```

This example uses the **item** method to get a collection of the children of the document body.

``` html
<script language="JScript">
var oItem = document.body.children;
if (oItem!=null) {
    for (i=0; i<oItem.length; i++)
        console.log(oItem.item(i).tagName);
}
</script>
```

## <span>Notes</span>

### <span>Remarks</span>

The **item** method cannot retrieve **input type=image** elements from a **form**. To access all elements contained in a form, use the [**children**](/dom/Element/children) collection. Windows Internet Explorer 8 and later. In IE8 Standards mode, the *index* parameter is not used. For more information, see Defining Document Compatibility.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
