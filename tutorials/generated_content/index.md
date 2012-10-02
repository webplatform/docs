{{Page_Title|Generating content with CSS}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article describes generated content — away in which you can use CSS to add content when a document is displayed.}}
{{Tutorial
|Content=== Information: Content ==
 
One of the important advantages of CSS is that it helps you to separate a document's style from its content. Yet there are situations where it makes sense to specify certain content as part of the stylesheet, not as part of the document. Content specified in a stylesheet can consist of text or images. You specify content in your stylesheet when the content is closely linked to the document's structure.

  
==Generated content in detail==
 
Specifying content in a stylesheet can cause complications. For example, you might have different language versions of your document that share a stylesheet. If part of the stylesheet has to be translated, it means that you must put those parts of the stylesheet in separate files and arrange for them to be linked with the appropriate language versions of your document.

These complications do not arise if the content you specify consists of symbols or images that apply in all languages and cultures.
 
Content specified in a stylesheet does not become part of the DOM.
  
=== Text content ===
 
CSS can insert text content before or after an element. To specify this, make a rule and add {{ cssxref(":before") }} or {{ cssxref(":after") }} to the selector. In the declaration, specify the {{ cssxref("content") }} property with the text content as its value.

====Generated text example==== 

This rule adds the text Reference: before every element with the class <code>ref</code>:

<pre>.ref:before {
  font-weight: bold;
  color: navy;
  content: "Reference: ";
}</pre>
   
==== More details==== 
The character set of a stylesheet is UTF-8 by default, but it can be specified in the link, or in the stylesheet itself, or in other ways. For details, see [[4.4 CSS style sheet representation]] in the CSS Specification.

Individual characters can also be specified by an escape mechanism that uses backslash as the escape character. For example, \265B is the chess symbol for a black queen ♛. For details, see [[Referring to characters not represented in a character encoding]] and also [[Characters and case]] in the CSS Specification.
  
=== Generated images===
 
To add an image before or after an element, you can specify the URL of an image file in the value of the {{ cssxref("content") }} property.

====Generated image example====

This rule adds a space and an icon after every link that has the class <code>glossary</code>:
 
<pre>a.glossary:after {content: " " url("../images/glossary-icon.gif");}</pre>
  
To add an image as an element's background, specify the URL of an image file in the value of the {{ cssxref("background") }} property. This is a shorthand property that specifies the background color, the image, how the image repeats, and some other details.
  
The following element rule sets the background of a specific element, using a URL to specify an image file. The selector specifies the element's id. The value <code>no-repeat</code> makes the image appear only once:
 
<pre>#sidebar-box {background: url("../images/sidebar-ground.png") no-repeat;}</pre>
   
====More details====
 
For information about individual properties affecting backgrounds, and about other options when you specify background images, see the {{ cssxref("background") }} reference page.
  
== Action: Adding a background image ==
 
This image is a white square with a blue line at the bottom:
     
[[Image:=Blue-rule.png|Image:Blue-rule.png]]

<ol> 
<li><p>Download the image file into the same directory as your CSS file. (For example, right-click it to get a context menu, then choose Save Image As and specify the directory that you are using for this tutorial.)</p></li>
<li><p>Edit your CSS file and add this rule to the body, setting a background image for the entire page.</p>

<pre>background: url("Blue-rule.png");</pre>
</li>
</ol>

<p>The value <code>repeat</code> is the default, so it does not need to be specified. The image repeats horizontally and vertically, giving an appearance like lined writing paper:</p>

[[Image:=Blue-rule-ground.png|Image:Blue-rule-ground.png]]     '''C'''ascading '''S'''tyle '''S'''heets     '''C'''ascading '''S'''tyle '''S'''heets
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Exercise question===

<ol> 
<li><p>Download this image:</p>

[[Image:=Yellow-pin.png|Image:Yellow-pin.png]] 
</li>
<li>
<p>Add a one rule to your stylesheet so that it displays the image at the start of each line:</p>
  
[[Image:=Blue-rule-ground.png|Image:Blue-rule-ground.png]]
</li>
</ol>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Content
|MSDN_link=
|HTML5Rocks_link=
}}