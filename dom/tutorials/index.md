{{Page_Title|Document Object Model tutorials}}
{{Flags
|State=Not Ready
|Editorial notes=No content; deletion candidate
|Checked_Out=No
}}
{{Summary_Section|This page lists tutorials designed to teach you all the concepts and practical techniques you'll need to know to do DOM manipulation.}}
{{Basic Page}}
==Introduction to Document Object Model==

DOM is an interface to interact with the contents of a webpage. All elements in a webpage can be described in a Document Object Model (DOM). What this means is that every HTML or SVG document can be represented as a tree of '''objects'''.  This object model is commonly used with JavaScript to create dynamic HTML.  In a DOM, all the HTML elements of a webpage like tags, attributes, comments and content are divided into the units called '''Nodes'''.

A DOM consists of a document structure and a set of interfaces that allow you to perform operations on each node of the document

For example, tags are called '''element nodes''' and attributes of a tag are called '''attribute nodes''', similarly text data are called '''text nodes''' and comments are called '''comments nodes''' and so on.



Look at the following code :

<syntaxhighlight lang="html5">
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
</syntaxhighlight>

The DOM tree structure for this code would be something like this :

[[File:DOM_1.svg]]


The DOM follows a hierarchical structure.

In the example, the <code>body</code> tag is the parent node of the <code>h1</code> and <code>p</code> tags because they are described inside the <code>body</code> tag. Similarly the <code>html</code> tag is the''' parent node''' of the <code>body</code> tag.

The <code>p</code> tags and the <code>h1</code> tags have a common parent in the <code>body</code> tag. When this happens the tags are called '''sibling nodes'''.

All the nodes located under a certain node are descendant nodes, and a node located
on the top of the parent nodes is an ancestor node.

==JavaScript HTML DOM Interface==
 
The Document Object Model is a W3C standard and categorized as:

* XML DOM
* Core DOM 
* HTML DOM
In this section we will be looking at the HTML DOM which is used to interact with the HTML elements.
To change something in html we use document methods, they are the primary way of interacting with the HTML. Let’s start of with an easy one. 

== The getElementsByTagName() method==

Firstly, pay attention to the syntax. The hardest part of learning JavaScript is the syntax, which is case sensitive. The getElementsByTagName() method retrieves a node by the given tag name.

Look at the following code: 

<syntaxhighlight lang="html5">
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

</syntaxhighlight>

This code is designed to change the CSS of the first <code>p</code> tag in the example. If we wanted to modify the CSS of the second p tag, you will need to change the p[0] to p[1]. The third p tag would then be p[2] and so on. This is because, in Javascript we start counting from 0.  This method sounds awfully inconvenient, especially if we have a HTML document with hundreds of tags.  So instead, let’s use a different method.

==The getElementById() method==

This is the most common method used to access HTML elements by using their id. In the following example we are modifying the font size of the text in the <code>p</code> tag with the id '''demo'''.


<syntaxhighlight lang="html5">
<html>
<head>
<title>Using getElementById Method</title>
<script type="text/javascript">
function changeSize(size){
 document.getElementById("demo").style.fontSize = size;
 </script>
</head>
 <body>
 <p>fontsize :
 <input type="button" value="small" onclick="changeSize('60%');">
<input type="button" value="normal" onclick="changeSize('100%');">
 <input type="button" value="big" onclick="changeSize('140%');">
 </p>
 
 <p id="demo">This is a random sentence</p>
 </body>
 </html>


</syntaxhighlight>


==The getElementsByClassName() method==

Similar to the getElementById() method, this method is used to select a whole class.

<syntaxhighlight lang="html5">
<html>
<head>
<title>Using the getElementsByClassName method</title>
<script type="text/javascript">
function changeSize(size){
 document.getElementsByClassName("demo").style.fontSize = size;
 </script>
</head>
 <body>
 <p>fontsize :
 <input type="button" value="small" onclick="changeSize('60%');">
<input type="button" value="normal" onclick="changeSize('100%');">
 <input type="button" value="big" onclick="changeSize('140%');">
 </p>
 
 <p class="demo">This is a random sentence</p>
<p class="demo">This is also another random sentence</p>
<div class="demo">Since this is a class, you can use it multiple times across different tags</div>
 </body>
 </html>
</syntaxhighlight>

==Modifying Attributes Methods==

{| class="wikitable"
|-
! Method Name
! Description
|-
| getAttribute()
| Used to retrieve an attribute value
|-
| setAttribute()
| Used to assign an attribute to an element
|- 
| removeAttribute()
| Used to remove an attribute from an element
|}

* '''getAttribute()'''

Syntax for this method is as follows:

<syntaxhighlight lang="javascript">

Variable = element.node.getAttribute("attribute name", "attribute value");
</syntaxhighlight>

<syntaxhighlight lang="javascript">

var x = document.getElementsByTagName("p")[0].getAttribute("align");
</syntaxhighlight>

* '''setAttribute()'''

Syntax for this method is as follows:

<syntaxhighlight lang="javascript">

element.node.setAttribute("attribute name", "attribute value");
</syntaxhighlight>

<syntaxhighlight lang="javascript">

document.getElementsByTagName("p")[0].setAttribute("align","right");
</syntaxhighlight>

This method is often used with event handlers like onclick() or onmouseover() to change an aspect of a website based on user input.

* '''removeAttribute()'''

Syntax for this method is as follows:

<syntaxhighlight lang="javascript">

element.node.removeAttribute("attribute name");
</syntaxhighlight>

<syntaxhighlight lang="javascript">

document.getElementsByTagName("p")[0].removeAttribute("align");
</syntaxhighlight>

Let's look at a quick example of these attributes in action:

<syntaxhighlight lang="html5">
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

</syntaxhighlight>

In the example above, using event handlers we are able to change the font size of the text based on mouse movement.

== Node Interface==

{| class="wikitable"
|-
! Node Property
! Description
|-
| nodeType
| Shows the node type
|-
| parentNode
| Access the parent node
|- 
| childNodes
| List of all the child nodes
|- 
| firstChild
| Selects the first child of the node
|- 
| lastChild
| Selects the last child of this node
|- 
| previousSibling
| Selects the node just before the current node
|- 
| nextSibling
| Selects the node just after the current node
|- 
| attributes
| Lists all the attributes in case of an element node
|- 
|}

Before we get started on this part, let's understand the node interface. In DOM every single piece of data can be viewed as a node. 

Let's look at this piece of code: 

<syntaxhighlight lang="html5">
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
</syntaxhighlight>

<syntaxhighlight lang="javascript">
document.getElementsByTagName("h1")[0].previousSibling.data="I am now the main heading";
</syntaxhighlight>

This will add the line before the h1 tag, Similartly the other commands behave as described. 

For the firstChild and a lastChild node properties,, sometimes when there is only one child in a node, in which case it is considered as the firstChild and the lastChild of that node.

What exactly is a child? It would probably be easier to explain in example form:
<syntaxhighlight lang="html5">
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
	   <input type="button" value="click" onclick="firstc()">
           <input type="button" value="click" onclick="lastc()">
       
</body>
</html>
</syntaxhighlight>

==Adding and Deleting Elements ==

So far we have seen how to manipulate html tags that have already been declared in the document, but now let's create some. (and then get rid of them).

{| class="wikitable"
|-
! Method Name
! Description
|-
| createElement()
| Used to create an element
|-
| removeChild()
| Remove the selected element or child node.
|- 
| appendChild()
| Add an element or child node.
|- 
| replaceChild()
| Replace an element or child node
|- 
|}

{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
}}