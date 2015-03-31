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