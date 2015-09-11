---
title: createElement
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/createElement.htm'
notes:
  - 'Needs mobile compat and links fixed at the bottom'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: Element
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Creates an instance of the element for the specified tag.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createElement

---
## <span>Summary</span>

Creates an instance of the element for the specified tag.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var element = document.createElement(tagName);
```

## <span>Parameters</span>

### <span>tagName</span>

 Data-type
:   String

 The name of an element. The element may be be an existing DOM element or an extension of a DOM element.

## <span>Return Value</span>

Returns an object of type ElementElement

The created element.

## <span>Examples</span>

This example uses the **createElement** method to dynamically update the contents of a Web page by adding an element selected from a drop-down list box.

``` html
<!doctype html>
<html>
 <head>
  <script>
function create() {
  var output, option, newElement, tagSelect, contentSelect;
  tagSelect = document.getElementById("tag-select");
  contentSelect = document.getElementById("content-select");
  output = document.getElementById("output");
  output.innerHTML = "";
  option = tagSelect.options[tagSelect.selectedIndex];
  if (option.text.length > 0) {
    newElement = document.createElement(option.textContent);
    newElement[option.value] = contentSelect.value;
    if (option.textContent === "a") {
      newElement.href = "http://www.bing.com";
    }
  }
  output.appendChild(newElement);
}
document.addEventListener("change", create, false);
  </script>
 </head>
 <body>
  <select id="tag-select">
   <option value="textContent">a</option>
   <option value="value">textarea</option>
  </select>
  <select id="content-select">
   <option></option>
   <option value="Text">Text</option>
   <option value="More and More Text">More and More Text</option>
  </select>
  <span id="output"></span>
 <body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/createElement.htm)

## <span>Usage</span>

     The properties of these created elements are read/write and can be accessed programmatically. Before you use new objects, you must explicitly add them to their respective collections or to the document. To insert new elements into the current document, use the insertBefore method or the appendChild method.

## <span>Notes</span>

You must perform a second step when you use **createElement** to create the [**input**](/html/elements/input) element. The **createElement** method generates an input text box, because that is the default **input** [**type**](/html/attributes/type) property. To insert any other kind of **input** element, first invoke **createElement** for **input**, and then set the **type** property to the appropriate value in the next line of code.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-2141741547)
:   Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Reference`
-   `cloneNode`
-   `Conceptual`
-   `About the W3C Document Object Model`
