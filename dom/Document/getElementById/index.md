{{Method
|Class=DOM
|API=element = document.getElementById(id);
|Summary=Returns a reference to the element by its ID.
|Sample call=<!DOCTYPE HTML>
<html>
<head>
  <title>getElementById example</title>
  <script>
  function changeColor(newColor)
  {
    var elem = document.getElementById("para1");
    elem.style.color = newColor;
  }
  </script>
</head>
<body>
  <p id="para1">Some text here</p>
  <button onclick="changeColor('blue');">blue</button>
  <button onclick="changeColor('red');">red</button>
</body>
</html>
|Return value=element
|See also=id, getElementsByTagName
}}
==Notes==

New users should note that the capitalization of 'Id' in the name of this method must be correct for the code to function - 'getElementByID' does not work, however natural it may seem.

If there is no element with the given id, this function returns null. Note that the ID parameter is case-sensitive, so document.getElementById("Main") will return null instead of the element <div id="main"> because "M" and "m" are different for the purposes of this method.

Elements not in the document are not searched by getElementById. When creating an element and assigning it an ID, you have to insert the element into the document tree with insertBefore or a similar method before you can access it with getElementById:
view plainprint?

    var element = document.createElement("div");  
    element.id = 'testqq';  
    var el = document.getElementById('testqq'); // el will be null!  

Non-HTML documents. The DOM implementation must have information that says which attributes are of type ID. Attributes with the name "id" are not of type ID unless so defined in the document's DTD. The id attribute is defined to be of ID type in the common cases of XHTML, XUL, and other. Implementations that do not know whether attributes are of type ID or not are expected to return null.