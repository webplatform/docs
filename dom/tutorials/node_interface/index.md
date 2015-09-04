---
title: node interface
uri: 'dom/tutorials/node interface'

---
## Node Interface

Node Property
:   Description
nodeType
:   Shows the node type
parentNode
:   Access the parent node
childNodes
:   List of all the child nodes
firstChild
:   Selects the first child of the node
lastChild
:   Selects the last child of this node
previousSibling
:   Selects the node just before the current node
nextSibling
:   Selects the node just after the current node
attributes
:   Lists all the attributes in case of an element node

Before we get started on this part, let's understand the node interface. In DOM every single piece of data can be viewed as a node.

Let's look at this piece of code:

``` {.html}
<html>
<head>
          <title>DOM</title>
</head>
<body>
         <h1>My Heading</h1>
          <p>Hello World!</p>
          <p>This is DOM</p>
</body>
</html>
```

 If we add this script to the HTML code:

``` {.js}
document.getElementsByTagName("h1")[0].previousSibling.data="I am now the main heading";
```

 It will appear in a line before the h1 tag, Similarly the other commands behave as described.

For the firstChild and a lastChild node properties,, sometimes when there is only one child in a node, in which case it is considered as the firstChild and the lastChild of that node.

It would probably be easier to explain in example form:

``` {.html}
<html>
<head>
<title>First Child, Last Chold</title>
</head>

<script type="text/javascript">
function firstc(){
document.getElementsByTagName("p")[0].firstChild.data="Pie";
document.getElementsByTagName("p")[1].firstChild.data="Pie";
document.getElementsByTagName("p")[2].firstChild.data="Pie";

}

function lastc(){
document.getElementsByTagName("p")[0].lastChild.data="cake";
document.getElementsByTagName("p")[1].lastChild.data="cake";
document.getElementsByTagName("p")[2].lastChild.data="cake";

}
</script>

<body>

       <p>first<em>Second</em>Third<em>Fourth</em>last</p>
       <p>First<em>Second</em>Last</p>
       <p>First and Last</p>
       <input type="button" value="First" onclick="firstc()">
           <input type="button" value="Last" onclick="lastc()">

</body>
</html>
```

[Next Tutorial: Adding and Deleting Elements](/dom/tutorials/adding_and_deleting_elements)