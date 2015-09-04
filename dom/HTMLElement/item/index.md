---
title: item
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'needs summary, clean-up of MSDN import'
uri: dom/HTMLElement/item

---
# item

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLElement](/dom/HTMLElement)*

## Syntax

``` {.js}
var object = object.item(name, index);
```

## Parameters

### name

 Data-typeÂ
:   VARIANT

**Variant** of type **Integer** or **String** that specifies the object or collection to retrieve. If this parameter is an integer, it is the zero-based index of the object. If this parameter is a string, all objects with matching [**name**](/html/attributes/name) or [**id**](/html/attributes/id) properties are retrieved, and a collection is returned if more than one match is made.

### index

 Data-typeÂ
:   VARIANT

**Variant** of type **Integer**Â that specifies the zero-based index of the object to retrieve when a collection is returned.

## Return Value

Returns an object of type DOM Node.

Object

## Examples

The following example uses the **item** method to retrieve each object from the document. In this case, the method parameter is a number, so the objects are retrieved in the order they appear in the document.

    <script language="JScript">
    var coll = document.all;
    if (coll!=null) {
        for (i=0; i<coll.length; i++)
            console.log(coll.item(i).tagName);
    }
    </script>

The next example uses the **item** method to retrieve a collection of all objects in the document that have "Sample" as an [**ID**](/html/attributes/id). The example then uses **item** again to retrieve each object from the "Sample" collection.

    <script language="JScript">
    var coll = document.all.item("Sample");
    If (collÂ != null) {
        for (i=0; i<coll.length; i++) {
            console.log(coll.item(i).tagName);
        }
    }
    </script>

The last example is similar to the previous example, but uses the optional *index* parameter of **item** to retrieve individual objects.

    <script language="JScript">
    var coll = document.all.item("Sample")
    if (coll!=null) {
        for (i=0; i<coll.length; i++)
            console.log(document.all.item("Sample",i).tagName);
    }
    </script>

This example uses the **item** method to get a collection of the children of the document body.

    <script language="JScript">
    var oItem = document.body.children;
    if (oItem!=null) {
        for (i=0; i<oItem.length; i++)
            console.log(oItem.item(i).tagName);
    }
    </script>

## Notes

### Remarks

The **item** method cannot retrieve **input type=image** elements from a **form**. To access all elements contained in a form, use the [**children**](/dom/Element/children) collection. Windows Internet ExplorerÂ 8 and later. In IE8 Standards mode, the *index* parameter is not used. For more information, see Defining Document Compatibility.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

