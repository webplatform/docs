---
title: getElementsByName
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat tables'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Returns an HTMLCollection of elements in the document that have a name attribute with the specified value.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/getElementsByName

---
## <span>Summary</span>

Returns an HTMLCollection of elements in the document that have a name attribute with the specified value.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var elementList = document.getElementsByName(name);
```

## <span>Parameters</span>

### <span>name</span>

 Data-type
:   String

 The value of a [**name**](/html/attributes/name) attribute.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

A list of elements with the a name attribute that matches the specified value.

## <span>Examples</span>

This example uses the **getElementsByName** method to return a collection of **input type=text** elements with the specified [**name**](/html/attributes/name) attribute value, `firstName`.

``` html
<script>
function getFirstNames() {
   // Prints a collection with 2 input type=text elements.
   console.log(document.getElementsByName("firstName"));
}
</script>
<input type="text" name="firstName"/>
<input type="text" name="firstName"/>
<input type="button" value="Get Names" onclick="getFirstNames()">
```

## <span>Related specifications</span>

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-71555259)
:   Recommendation

[W3C HTML5](http://www.w3.org/html/wg/drafts/html/master/single-page.html)
:   Editor's Draft
