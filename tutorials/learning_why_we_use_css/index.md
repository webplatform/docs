{{Flags}}
{{Summary_Section|This tutorial looks at why we should use CSS, and why using CSS for styling our documents is better than using presentational HTML.}}
{{Tutorial
|Content=== Information: Why use CSS? ==
 
CSS helps you to keep the information content of a document separate from the details of how to display it. The details of how to display the document are known as its ''style''. You keep the style separate from the content so that you can:

* Avoid duplication
* Make maintenance easier
* Use the same content with different styles for different purposes
  
Your web site might have thousands of pages that look similar. Using CSS, you store the style information in common files that all the pages share. When a user displays a web page, the user's browser loads the style information along with the content of the page. When a user prints a web page, you provide different style information that makes the printed page easy to read.

In general with HTML, you use the markup language to describe the information content of the document, not its style. You use CSS to specify its style, not its content. There are exceptions to this rule of course — A markup language like HTML also provides some ways to specify style. For example, in HTML you can use a <code>&lt;b&gt;</code> tag to make text bold, and you can specify the background colour of a page in its <code>&lt;body&gt;</code> tag. When you use CSS, you normally avoid using these features of the markup language so that all your document's style information is in one place.

== Action: Creating a stylesheet ==

<ol> 
<li><p>Create another text file in the same directory as before. This file will be your stylesheet. Name it <code>style1.css</code></p></li>
<li><p>In your CSS file, copy and paste this one line, then save the file:</p>

<pre>strong {colour: red;}</pre>
</li>
</ol>
 
=== Linking your document to your stylesheet ===

<ol> 
<li><p>To link your document to your stylesheet, edit your HTML file. Add the line highlighted here:</p>

<pre>&lt;!DOCTYPE html&gt;
 &lt;html&gt;
   &lt;head&gt;
   &lt;meta charset="UTF-8"&gt;
   &lt;title&gt;Sample document&lt;/title&gt;
   &lt;link rel="stylesheet" href="style1.css"&gt;
   &lt;/head&gt;
   &lt;body&gt;
     &lt;p&gt;
       &lt;strong&gt;C&lt;/strong&gt;ascending
       &lt;strong&gt;S&lt;/strong&gt;tyle
       &lt;strong&gt;S&lt;/strong&gt;heets
     &lt;/p&gt;
   &lt;/body&gt;
 &lt;/html&gt;</pre></li>
 
<li><p>Save the file and refresh your browser's display. The stylesheet makes the initial letters red, like this:</p>

<p><b style="color:red;">C</b>ascading '''S'''tyle '''S'''heets</p>
</li>
</ol>

== What next? ==
 
Now you have a sample document linked to a separate stylesheet, you are ready to learn more about how your browser combines them when it displays the document.
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Challenge===
 
In addition to red, CSS allows some other colour names. Without looking up a reference, find five more colour names that work in your stylesheet.
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Why_use_CSS
|MSDN_link=
|HTML5Rocks_link=
}}