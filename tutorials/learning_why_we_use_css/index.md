{{Page_Title|Why use CSS?}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Byline
|Name=
|URL=
|Published=
}}
{{Summary_Section|This tutorial looks at why we should use CSS, and why using CSS for styling our documents is better than using presentational HTML.}}
{{Tutorial
|Next_page=
|Prev_page=
|Content=== Information: Why use CSS? ==
 
CSS helps you to keep the informational content of a document separate from the details of how to display it. The details of how to display the 
document are known as its ''style''. You keep the style separate from the content so that you can:

* Avoid duplication
* Make maintenance easier
* Use the same content with different styles for different purposes
  
Your web site might have thousands of pages that look similar. Using CSS, you store the style information in common files that all the pages share. 
When a user displays a web page, the user's browser loads the style information along with the content of the page. 
When a user prints a web page, you might provide different style information that makes the printed page easy to read.

In general, you use HTML to describe the content of the document, not its style; you use CSS to specify its style, not its content. 
There are exceptions to this rule, of course, and HTML also provides some ways to specify style. For example, in HTML you can use a 
<code>&lt;b&gt;</code> tag to make text bold, and you can specify the background colour of a page in its <code>&lt;body&gt;</code> tag. 
When you use CSS, you normally avoid using these HTML style features so that all your document's style information is in one place.

== Action: Creating a style sheet for an HTML document ==

===Creating the style sheet===
<ol> 
<li><p>Create a text file; this file will be your style sheet. Name it <code>style1.css</code></p></li>
<li><p>In your CSS file, copy and paste this one line, then save the file:</p>

<syntaxhighlight lang="css">strong { color: red; }</syntaxhighlight>
</li>
</ol>
 
=== Linking your document to your stylesheet ===
<ol> 
<li><p>Create another text file; this file will be your HTML document. Name it whatever you like.</p></li>
<li><p>In your HTML file, copy and paste the following lines; the &lt;link...&gt; line references your style sheet:</p>

<syntaxhighlight lang="html5"><!DOCTYPE html>
 <html>
   <head>
   <meta charset="UTF-8">
   <title>Sample document</title>
   <link rel="stylesheet" href="style1.css">
   </head>
   <body>
     <p>
       <strong>C</strong>ascading
       <strong>S</strong>tyle
       <strong>S</strong>heets
     </p>
   </body>
 </html></syntaxhighlight></li>
 
<li><p>Save the file and load it in a browser. The style sheet makes the initial letters red, like this:</p>

<p><b style="color:red;">C</b>ascading <b style="color:red;">S</b>tyle <b style="color:red;">S</b>heets</p>
</li>
</ol>

== What next? ==
 
Now you have a sample document linked to a separate style sheet, you are ready to learn more about how your browser combines them when it displays the document. See the other tutorials in this section for more information.

}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Why_use_CSS
|MSDN_link=
|HTML5Rocks_link=
}}