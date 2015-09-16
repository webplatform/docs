---
title: getelementsmethod
uri: dom/tutorials/getelementsmethod

---
## JavaScript HTML DOM Interface

The Document Object Model is a W3C standard and categorized as:

-   XML DOM
-   Core DOM
-   HTML DOM

In this section we will be looking at the HTML DOM which is used to interact with the HTML elements. To change something in html we use document methods, they are the primary way of interacting with the HTML. Let’s start of with an easy one.

## The getElementsByTagName() method

Firstly, pay attention to the syntax. The hardest part of learning JavaScript is the syntax, which is case sensitive. The getElementsByTagName() method retrieves a node by the given tag name.

Look at the following code:

``` html
<html>
<head>
  <title>Specify CSS style</title>
  <script type="text/javascript">
    function changeSize(){
      document.getElementsByTagName("p")[0].style.fontSize = "140%";
      document.getElementsByTagName("p")[1].style.fontSize = "160%";
    }
  </script>
</head>

<body>
  <input type="button" value="Click" onclick="changeSize();">
  <p>Paragraph 1</p>
  <p>Paragraph 2</p>

</body>
</html>
```

 This code is designed to change the CSS of the first `p` tag in the example. If we wanted to modify the CSS of the second p tag, you will need to change the p[0] to p[1]. The third p tag would then be p[2] and so on. This is because, in Javascript we start counting from 0. This method sounds awfully inconvenient, especially if we have a HTML document with hundreds of tags. So instead, let’s use a different method.

## The getElementById() method

This is the most common method used to access HTML elements by using their id. In the following example we are modifying the font size of the text in the `p` tag with the id **demo**.

``` html
<html>
<head>
  <title>Using getElementById Method</title>
  <script type="text/javascript">
    function changeSize(size){
      document.getElementById("demo").style.fontSize = size;
    }
  </script>
</head>

<body>
  <p>fontsize :
    <input type="button" value="small" onclick="changeSize('60%');">
    <input type="button" value="normal" onclick="changeSize('100%');">
    <input type="button" value="big" onclick="changeSize('140%');">
  </p>

  <p id="demo">This is a random sentence</p>

</body>
</html>
```

## The getElementsByClassName() method

Similar to the getElementById() method, this method is used to select a whole class.

``` html
<html>
<head>
  <title>Using the getElementsByClassName method</title>
  <script type="text/javascript">
    function changeSize(size){
      document.getElementsByClassName("demo").style.fontSize = size;
    }
  </script>
</head>

<body>
  <p>fontsize :
    <input type="button" value="small" onclick="changeSize('60%');">
    <input type="button" value="normal" onclick="changeSize('100%');">
    <input type="button" value="big" onclick="changeSize('140%');">
  </p>

  <p class="demo">This is a random sentence</p>
  <p class="demo">This is also another random sentence</p>
  <div class="demo">Since this is a class, you can use it multiple times across different tags</div>

</body>
</html>
```

[Next Tutorial: Attribute Methods](/dom/tutorials/attribute_methods)
