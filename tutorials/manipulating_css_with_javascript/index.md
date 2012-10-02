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
 
<ol>
<li>
<p>Make a new HTML document, <code>doc5.html</code>. Copy and paste the content from here, making sure that you scroll to get all of it:
  
<pre>&lt;!DOCTYPE html&gt;
&lt;html&gt;

&lt;head&gt;
&lt;title&gt;Mozilla CSS Getting Started - JavaScript demonstration&lt;/title&gt;
&lt;link rel="stylesheet" type="text/css" href="style5.css" /&gt;
&lt;script type="text/javascript" src="script5.js"&gt;&lt;/script&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;h1&gt;JavaScript sample&lt;/h1&gt;

&lt;div id="square"&gt;&lt;/div&gt;

&lt;button type="button" onclick="doDemo(this);"&gt;Click Me&lt;/button&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>
</li>
<li>
<p>Make a new CSS file, <code>style5.css</code>. Copy and paste the content from here:</p>

<pre>/*** JavaScript demonstration ***/
#square {
  width: 20em;
  height: 20em;
  border: 2px inset gray;
  margin-bottom: 1em;
}

button {
  padding: .5em 2em;
}</pre>
</li>
<li>
<p>Make a new text file, <code>script5.js</code>. Copy and paste the content from here:</p>

<pre>// JavaScript demonstration
function doDemo (button) {
  var square = document.getElementById("square");
  square.style.backgroundColor = "#fa4";
  button.setAttribute("disabled", "true");
  setTimeout(clearDemo, 2000, button);
}

function clearDemo (button) {
  var square = document.getElementById("square");
  square.style.backgroundColor = "transparent";
  button.removeAttribute("disabled");
}</pre>
</li>
<li>
<p>Open the document in your browser and press the button.</p>
</li>
</ol>

<p class="note">add a dabblet to show what happens here, or before and after screenshot?</p>
  
Notes on what is happening in the above example:

* The HTML document links the stylesheet as usual, and it also links the script.
* The script works with individual elements in the DOM. It modifies the square's style directly. It modifies the button's style indirectly by changing an attribute.
* In JavaScript, <code>document.getElementById("square")</code> is similar in function to to the CSS selector <code>#square</code>.
* In JavaScript, <code>backgroundColor</code> corresponds to the CSS property <code>background-color</code>. JavaScript does not allow hyphens in names, so "camelCase" is used instead.
* Your browser has a built-in CSS rule for <code>button{{ mediawiki.external('disabled=\"true\"') }}</code> that changes the button's appearance when it is disabled.
}}
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
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/JavaScript
|MSDN_link=
|HTML5Rocks_link=
}}