---
title: 'attribute methods'
uri: 'dom/tutorials/attribute methods'

---
## Modifying Attributes Methods

|Method Name|Description|
|:----------|:----------|
|getAttribute()|Used to retrieve an attribute value|
|setAttribute()|Used to assign an attribute to an element|
|removeAttribute()|Used to remove an attribute from an element|

-   **getAttribute()**

Syntax for this method is as follows:

``` js
Variable = element.node.getAttribute("attribute name", "attribute value");
```

``` js
var x = document.getElementsByTagName("p")[0].getAttribute("align");
```

-   **setAttribute()**

Syntax for this method is as follows:

``` js
element.node.setAttribute("attribute name", "attribute value");
```

``` js
document.getElementsByTagName("p")[0].setAttribute("align","right");
```

 This method is often used with event handlers like onclick() or onmouseover() to change an aspect of a website based on user input.

-   **removeAttribute()**

Syntax for this method is as follows:

``` js
element.node.removeAttribute("attribute name");
```

``` js
document.getElementsByTagName("p")[0].removeAttribute("align");
```

 Let's look at a quick example of these attributes in action:

``` html
<html>
<head>
  <title>Setting and removing attributes</title>

  <script type="text/javascript">
   function onmousefont(){
    document.getElementsByTagName("font")[0].setAttribute("size","7");
   }
   function offmousefont(){
    document.getElementsByTagName("font")[0].removeAttribute("size");
   }
</script>

</head>
<body>
   <font onmouseover="onmousefont();" onmouseout="offmousefont();">Mouse over me! </font>
</body>
</html>
```

 In the example above, using event handlers we are able to change the font size of the text based on mouse movement.

[Next Tutorial: Node Interface](/dom/tutorials/node_interface)
