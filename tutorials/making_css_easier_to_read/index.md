{{Flags}}
{{Summary_Section|This article looks at the style and grammar of the CSS language itself, and how to make your CSS more readable using whitespace and comments.}}
{{Tutorial
|Content=== Information: Readable CSS ==
 
You can add whitespace and comments to your stylesheets to make them more readable. You can also group selectors together, when the same style rules apply to elements selected in different ways.
 
=== White space ===
 
Whitespace means actual spaces, tabs and new lines. You can add white space to make your stylesheets more readable.

Your sample CSS files will currently have one rule per line, and almost the minimum of white space. In a complex stylesheet this layout would be difficult to read, making the stylesheet difficult to maintain.

The layout you choose is usually a personal preference, but if your stylesheets are part of shared projects, those projects might have their own conventions.

Some people like the compact layout that we have been using, only splitting a line when it becomes very long:

<pre>.carrot {color: orange; text-decoration: underline; font-style: italic;}</pre>
 
Some people prefer one property-value (selector, curly brace, etc.) per line:

<pre>.carrot
{
color: orange;
text-decoration: underline;
font-style: italic;
}</pre>

Some people prefer to put the first bracket on the same line as the selector:

<pre>.carrot {
  color: orange;
  text-decoration: underline;
  font-style: italic;
}</pre>
 
Some people use indention—two spaces, four spaces, or a tab are common:
 
<pre>.carrot {
  color: orange;
  text-decoration: underline;
  font-style: italic;
}</pre>
 
Some people like everything to line up vertically (but a layout like this is difficult to maintain):

<pre>.carrot
{
  color:                 orange;
  text-decoration:       underline;
  font-style:            italic;
}</pre>
  
Some people use tabs for the layout. Some people only use spaces.
 
=== Comments ===
 
Comments in CSS begin with <code>/*</code> and end with <code>*/</code>. You can use comments to make actual comments in your stylesheet, and also to ''comment out'' parts of it temporarily for testing purposes. To comment out part of a stylesheet, place that part in a comment so that the browser ignores it. Be careful where you start and end the comment. The rest of the stylesheet must still have correct syntax.

<pre>/* style for initial letter C in first paragraph */
.carrot {
  color: orange;
  text-decoration: underline;
  font-style: italic;
}</pre>
  
=== Grouped selectors ===
 
When many elements have the same style, you can specify a group of selectors, separating them with commas. The declaration applies to all the selected elements.

Elsewhere in your stylesheet you can specify the same selectors again individually, to apply individual style rules to them.

This rule makes [h1], [h2], and [h3] elements the same color — it is convenient to specify the color in only one place, in case it has to be changed:

<pre>/* color for headings */
h1, h2, h3 {color: navy;}
</pre>
  
== Action: Adding comments and improving the layout ==
 
<ul>
<li><p>Edit your CSS file, and ensure that it has these rules in it (in any order):<p>

<pre>strong {color: red;}
.carrot {color: orange;}
.spinach {color: green;}
#first {font-style: italic;}
p {color: blue;}</pre></li>
<li><p>Make it more readable by rearranging it in a way that you find logical, and by adding white space and comments in whatever way you think best.</p></li>
<li><p>Save the file and refresh your browser's display, to make sure that your changes do not affect how the stylesheet works.</p></li>

<p class="note">Need to add a screenshot to show what it should look like.</p>
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Exercise questions===

Comment out part of your stylesheet, without changing anything else, to make the very first letter of your document red.
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MSDN_link=
|HTML5Rocks_link=
}}