{{Page_Title|Manipulating CSS with JavaScript}}
{{Flags}}
{{Byline}}
{{Summary_Section|In this article we look at the basics of how to manipulate CSS styles using JavaScript.}}
{{Tutorial
|Content==== Information: JavaScript ===
 
JavaScript is a ''programming language''. JavaScript is widely used to provide interactivity in web sites and applications. JavaScript can interact with stylesheets, allowing you to write programs that change a document's style dynamically.

 
There are three ways to do this:

* By working with the document's list of stylesheets—for example: adding, removing or modifying a stylesheet.
* By working with the rules in a stylesheet—for example: adding, removing or modifying a rule.
* By working with an individual element in the DOM—modifying its style independently of the document's stylesheets
        
=== Action: A JavaScript demonstration ===
 
# Make a new HTML document, <code>doc5.html</code>. Copy and paste the content from here, making sure that you scroll to get all of it:
  
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html>

<head>
<title>Mozilla CSS Getting Started - JavaScript demonstration</title>
<link rel="stylesheet" type="text/css" href="style5.css" />
<script type="text/javascript" src="script5.js"></script>
</head>

<body>
<h1>JavaScript sample</h1>

<div id="square"></div>

<button type="button" onclick="doDemo(this);">Click Me</button>

</body>
</html>
</syntaxhighlight>

# Make a new CSS file, <code>style5.css</code>. Copy and paste the content from here:

<syntaxhighlight lang="css">
#square {
  width: 20em;
  height: 20em;
  border: 2px inset gray;
  margin-bottom: 1em;
}

button {
  padding: .5em 2em;
}</syntaxhighlight>


# <p>Make a new text file, <code>script5.js</code>. Copy and paste the content from here:</p>

<syntaxhighlight lang="javascript">// JavaScript demonstration

var square = document.getElementById("square"),
    clickMe = document.getElementById('clickMe'); //Keeping it unobstrusive

function doDemo () {

  var button = this;
  square.style.backgroundColor = "#fa4";
  button.setAttribute("disabled", "true");
  setTimeout(clearDemo, 2000, button); //After 2000 miliseconds, run clearDemo, which argument button.
}

function clearDemo (button) {
  var square = document.getElementById("square");
  square.style.backgroundColor = "transparent";
  button.removeAttribute("disabled");
}

clickMe.onclick = doDemo; //Onclick call. Pass no arguments.

</syntaxhighlight>


# Open the document in your browser and press the button.</p>


<p>What this code does, is that it changes the background color of the <code>#square</code> to <code>#ffaa44</code>. Here's a [http://jsfiddle.net/namanyayg/Angmu/1/ JSFiddle] so you can see it working live.</p>
  
Notes on what is happening in the above example:

* The HTML document links the stylesheet as usual, and it also links the script.
* The script works with individual elements in the DOM. It modifies the square's style directly. It modifies the button's style indirectly by changing an attribute.
* In JavaScript, <code>document.getElementById("square")</code> is similar in function to to the CSS selector <code>#square</code> and in a similar way, <code>document.getElementById('clickMe')</code> is similar to <code>#clickMe</code>.
* In JavaScript, <code>backgroundColor</code> corresponds to the CSS property <code>background-color</code>. JavaScript does not allow hyphens in names, so "camelCase" is used instead.
* Your browser has a built-in CSS rule for <code>button</code> that changes the button's appearance when it is disabled.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections===Exercise question==

Change the script so that the square jumps to the right by 20 em when its color changes, and jumps back afterwards.
}}
{{Topics|CSS, DOM, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/JavaScript
|MSDN_link=
|HTML5Rocks_link=
}}