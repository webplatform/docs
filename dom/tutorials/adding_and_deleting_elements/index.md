---
title: 'adding and deleting elements'
uri: 'dom/tutorials/adding and deleting elements'

---
## Adding and Deleting Elements

So far we have seen how to manipulate html tags that have already been declared in the document, but now let's create some. (and then get rid of them).

|Method Name|Description|
|:----------|:----------|
|createElement()|Used to create an element|
|removeChild()|Remove the selected element or child node.|
|appendChild()|Add an element or child node.|
|replaceChild()|Replace an element or child node|

-   **createElement()**

Syntax for this method is as follows:

``` js
Variable = element.createElement("element name");
```

``` js
var newimg = document.createElement("img");
```

 This will just create an image element. To display an image we must first set its attributes.

``` js
var newimg = document.createElement("img");
newimg.setAttribute("src", "abc.jpg");
```

-   **removeChild()**

Syntax for this method is as follows:

``` js
element.node.removeChild(node);
```

``` js
document.getElementsByTagName.removeChild(newimg);
```

-   **appendChild()**

Syntax for this method is as follows:

``` js
element.node.appendChild(node);
```

``` js
document.getElementsByTagName("p")[0].appendChild(newimg);
```

-   **replaceChild()**

The Syntax for this method is as follows:

``` js
node.replaceChild(newnode,oldnode);
```

 All right, lets look at these methods in action.

``` html
<html>
<head>

<script type="text/javascript">


function create(){

var createstuff = document.createElement("p");
createstuff.innerHTML="Stuff";
document.getElementById("container").appendChild(createstuff);


}

function destroy(){

var olddata=document.getElementById("container").lastChild;
document.getElementById("container").removeChild(olddata);

}
</script>

        <title>Javascript2_lesson11</title>

</head>
<body>
      <input type="button" value="Psst over here" onmouseover="create();" onmouseout="destroy();">

      <p id="container"></p>



</body>
</html>
```

 Ask yourself a few questions:

-   What is happening in the create() function?
-   What is happening in the destroy() function?
-   In the destroy() function, what happens if you replace :

``` js
var olddata=document.getElementById("container").lastChild;
```

with

``` js
var olddata=document.getElementById("container").firstChild;
```

 Now let's look at an example for replaceChild():

``` html
<html>
<head>
<title>replaceChild</title>
<script type="text/javascript">
function replaceit(){

var theoriginal = document.getElementById('ori');

var thereplacement = document.createElement('p');

thereplacement.appendChild(document.createTextNode('Replacement Text'));

theoriginal.replaceChild(thereplacement, theoriginal.lastChild);

}
</script>
</head>

<body>


<p id="ori">Original Text</p>
<input type="button" value="click" onclick="replaceit()">


</body>
</html>
```
