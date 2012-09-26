{{Flags}}
{{Summary_Section|This article shows how you can use CSS to style XML data.}}
{{Tutorial
|Content==== Information: XML data ===
 
''[[XML]]'' (eXtensible Markup Language) is a general-purpose language for any kind of structured data.

By default, your Mozilla browser displays XML in a format very similar to the original data in the XML file. You see the actual tags that define the data's structure.
 
By linking a CSS stylesheet with the XML document, you can define other ways to display it. To do this, your stylesheet uses rules that map tags in the XML document to the display types used by HTML.

Example

Data in an XML document uses <code>&lt;INFO&gt;</code> tags. You want the document's INFO elements to be displayed like HTML paragraphs.
        
In the document's stylesheet, you specify how INFO elements are to be displayed:

<pre>INFO {
  display: block;
  margin: 1em 0;
}</pre>
  
The most common values for the <code>display</code> property are:

{{{!}} border="1"
{{!}}-
{{!}}<code>block</code>
{{!}}Displayed like HTML's DIV (for headings, paragraphs)
{{!}}-
{{!}}<code>inline</code>
{{!}}Displayed like HTML's SPAN (for emphasis within text)
{{!}}} 

Add your own style rules that specify the font, spacing and other details in the same way as for HTML. Other values of <code>display</code> display the element like a list item, or like a component of a table.
        
For the full list of display types, see [[The display property]] in the CSS Specification. Using CSS alone, the structure of the display must be the same as the structure of the document. Other technologies can modify the structure of the display—for example, XBL can add content, and JavaScript can modify the DOM.
 
For more information about XML in Mozilla, see the [[XML]] page in this wiki.

=== Action: An XML demonstration ===

<ol>
<li>
<p>Make a new XML file, <code>doc9.xml</code>. Copy and paste the content from here, making sure that you scroll to get all of it:</p>
  
<pre>
&lt;?xml version="1.0"?&gt;
&lt;!-- XML demonstration --&gt;

&lt;?xml-stylesheet type="text/css" href="style9.css"?&gt;

&lt;!DOCTYPE planet&gt;
&lt;planet&gt;

&lt;ocean&gt;
&lt;name&gt;Arctic&lt;/name&gt;
&lt;area&gt;13,000&lt;/area&gt;
&lt;depth&gt;1,200&lt;/depth&gt;
&lt;/ocean&gt;

&lt;ocean&gt;
&lt;name&gt;Atlantic&lt;/name&gt;
&lt;area&gt;87,000&lt;/area&gt;
&lt;depth&gt;3,900&lt;/depth&gt;
&lt;/ocean&gt;

&lt;ocean&gt;
&lt;name&gt;Pacific&lt;/name&gt;
&lt;area&gt;180,000&lt;/area&gt;
&lt;depth&gt;4,000&lt;/depth&gt;
&lt;/ocean&gt;

&lt;ocean&gt;
&lt;name&gt;Indian&lt;/name&gt;
&lt;area&gt;75,000&lt;/area&gt;
&lt;depth&gt;3,900&lt;/depth&gt;
&lt;/ocean&gt;

&lt;ocean&gt;
&lt;name&gt;Southern&lt;/name&gt;
&lt;area&gt;20,000&lt;/area&gt;
&lt;depth&gt;4,500&lt;/depth&gt;
&lt;/ocean&gt;

&lt;/planet&gt;</pre>
</li>
<li>
<p>Make a new CSS file, <code>style9.css</code>. Copy and paste the content from here, making sure that you scroll to get all of it:</p>
  
<pre>/*** XML demonstration ***/

planet:before {
  display: block;
  width: 8em;
  font-weight: bold;
  font-size: 200%;
  content: "Oceans";
  margin: -.75em 0px .25em -.25em;
  padding: .1em .25em;
  background-color: #cdf;
  }

planet {
  display: block;
  margin: 2em 1em;
  border: 4px solid #cdf;
  padding: 0px 1em;
  background-color: white;
  }

ocean {
  display: block;
  margin-bottom: 1em;
  }

name {
  display: block;
  font-weight: bold;
  font-size: 150%;
  }

area {
  display: block;
  }

area:before {
  content: "Area: ";
  }

area:after {
  content: " million km\B2";
  }

depth {
  display: block;
  }

depth:before {
  content: "Mean depth: ";
  }

depth:after {
  content: " m";
}</pre>
</li>
<li>
<p>Open the document in your browser:</p>
<p class="note">Note: add dabblet or screenshot to show result</p>
 
Notes about this demonstration:
 
* The superscript 2 (in "million km²") a Unicode character, coded as <code>\B2</code> in the CSS file.
* The heading, "Oceans", has a negative top margin, moving it up so it is displayed on top of the border.
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections===Exercise question==

Change the stylesheet so that it displays the document as a table.
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/XML_data
|MSDN_link=
|HTML5Rocks_link=
}}