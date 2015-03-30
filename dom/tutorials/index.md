{{Page_Title|Document Object Model tutorials}}
{{Flags
|State=Not Ready
|Editorial notes=No content; deletion candidate
|Checked_Out=No
}}
{{Summary_Section|This page lists tutorials designed to teach you all the concepts and practical techniques you'll need to know to do DOM manipulation.}}
{{Basic Page}}
==Introduction to Document Object Model==

DOM is an interface to interact with the contents of a webpage. All elements in a webpage can be described in a Document Object Model (DOM). What this means is that every HTML document can be represented as a tree of “objects”.  This object model is commonly used with JavaScript to create dynamic HTML.  In a DOM, all the HTML elements of a webpage like tags, attributes, comments and content are divided into the units called “Nodes”.

For example, tags are called “element nodes” and attributes of a tag are called “attribute nodes”, similarly text data are called “text nodes” and comments are called “comments nodes” and so on.



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
--- DOM_1.svg-- (Dont have permission to upload images yet) :(

The DOM follows a hierarchical structure.

In the example, the <code>body</code> tag is the parent node of the <code>h1</code> and <code>p</code> tags because they are described inside the <code>body</code> tag. Similarly the <code>html</code> tag is the parent node of the <code>body</code> tag.

The <code>p</code> tags and the <code>h1</code> tags have a common parent in the <code>body</code> tag. When this happens the tags are called sibling nodes.

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
 function changecolor(){
 document.getElementsByTagName("p")[0].style.background = "silver"; 
 document.getElementsByTagName("p")[0].style.color = "green";
}
</script>
 </head>
 <body>
 <input type="button" value="Click" onclick="changecolor();">
<p>Paragraph 1</p>
<p>Paragraph 2</p>
</body>
 </html>

</syntaxhighlight>

This code is designed to change the CSS of the first <code>p</code> tag in the example. If we wanted to modify the CSS of the second p tag, you will need to change the p[0] to p[1]. The third p tag would then be p[2] and so on. This is because, in Javascript we start counting from 0.  This method sounds awfully inconvenient, especially if we have a HTML document with hundreds of tags.  So instead, let’s use a different method.

==The getElementById() method==

This is the most common method used to access HTML elements by using their id. In the following example we are modifying the font size of the text in the <code>p</code> tag with the id “demo”.


<syntaxhighlight lang="html5">
<html>
<head>
<title>Using getElementById Method</title>
<script type="text/javascript">
function changeFontSize(size){
 document.getElementById("demo").style.fontSize = size;
 </script>
</head>
 <body>
 <p>fontsize :
 <input type="button" value="small" onclick="changeFontSize('60%');">
<input type="button" value="normal" onclick="changeFontSize('100%');">
 <input type="button" value="big" onclick="changeFontSize('140%');">
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
function changeFontSize(size){
 document.getElementsByClassName("demo").style.fontSize = size;
 </script>
</head>
 <body>
 <p>fontsize :
 <input type="button" value="small" onclick="changeFontSize('60%');">
<input type="button" value="normal" onclick="changeFontSize('100%');">
 <input type="button" value="big" onclick="changeFontSize('140%');">
 </p>
 
 <p class="demo">This is a random sentence</p>
<p class="demo">This is also another random sentence</p>
<div class="demo">Since this is a class, you can use it multiple times across different tags</div>
 </body>
 </html>
</syntaxhighlight>
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
}}