{{Flags}}
{{Summary_Section|This article focuses on using media types to target CSS at different type of media — screen, print, etc.}}
{{Tutorial
|Content= == Information: Media ==
 
The purpose of CSS is to specify how documents are presented to the user. Presentation can take more than one form.

For example, you are probably reading this page on a display device. But you might also want to project it on a screen for a large audience, or print it. These different media can have different characteristics. CSS provides ways to present a document differently in different media.
 
To specify rules that are specific to a type of media, use <code>@media</code> followed by the media type, followed by curly braces that enclose the rules.
  
==Media type example==

A document on a web site has a navigation area to allow the user to move around the site.
 
In the markup language, the navigation area's parent element has the '''id''' <code>nav-area</code>. (In HTML5, this can be marked up with the [nav] element instead of [div] with an '''id''' attribute.)
 
When the document is printed the navigation area has no purpose, so the stylesheet removes it completely:
 
<pre>@media print {
  #nav-area {display: none;}
}</pre>
  
Some of the common media types are:
                    
{{{!}} border="1"
{{!}}-
{{!}}<code>screen</code>
{{!}}Color computer display
{{!}}-
{{!}}<code>print</code>
{{!}}Paged media
{{!}}-
{{!}}<code>projection</code>
{{!}}Projected display
{{!}}-
{{!}}<code>all</code>
{{!}}All media (the default)
{{!}}} 

==Different ways to specify media types==

There are other ways to specify the media type of a set of rules.
 
The document's markup language might allow the media type to be specified when the stylesheet is linked to the document. For example, in HTML you can optionally specify the media type with a <code>media</code> attribute in the <code>link</code> element.
 
In CSS you can use <code>@import</code> at the start of a stylesheet to import another stylesheet from a URL, optionally specifying the media type.
 
By using these techniques you can separate style rules for different media types into different files. This is sometimes a useful way to structure your stylesheets.
 
For full details of media types, see [[Media]] in the CSS Specification.
  
=== Printing ===
 
CSS has some specific support for printing and for paged media in general.
 
A [@page] rule can set the page margins. For double-sided printing, you can specify the margins separately for <code>@page:left</code> and <code>@page:right</code>.

 For print media, you normally use appropriate length units like inches (<code>in</code>) and points (<code>pt</code> = 1/72 inch), or centimeters (<code>cm</code>) and millimeters (<code>mm</code>). It is equally appropriate to use ems (<code>em</code>) to match the font size, and percentages (<code>%</code>).

You can control how the content of the document breaks across page boundaries, by using the [page-break-before], [page-break-after} and [page-break-inside] properties.

More examples 
This rule sets the page margins to one inch on all four sides:
 
<pre>@page {margin: 1in;}</pre>
  
This rule ensures that every H1 element starts on a new page:

<pre>h1 {page-break-before: always;}</pre>
   
More details 
For full details of CSS support for paged media, see [[Paged media]] in the CSS Specification.

Like other features of CSS, printing depends on your browser and its settings. For example, your Mozilla browser supplies default margins, headers and footers when it prints. When other users print your document, you probably cannot predict the browser and the settings that they will use, so you probably cannot control the results completely.

=== User interfaces ===
 
CSS has some special properties for devices that support a user interface, like computer displays. These make the document's appearance change dynamically as the user works with the interface. There is no special media type for devices with user interfaces.

There are five special selectors:

{{{!}} border="1"
{{!}}-
{{!}}'''Selector'''
{{!}}'''Selects'''
{{!}}-
{{!}}<code>E{{ cssxref(":hover") }}</code>
{{!}}Any E element that has the pointer over it
{{!}}-
{{!}}<code>E{{ cssxref(":focus") }}</code>
{{!}}Any E element that has keyboard focus
{{!}}-
{{!}}<code>E{{ cssxref(":active") }}</code>
{{!}}The E element that is involved in the current user action
{{!}}-
{{!}}<code>E{{ cssxref(":link") }}</code>
{{!}}Any E element that is a hyperlink to a URL that the user has ''not'' visited recently
{{!}}-
{{!}}<code>E{{ cssxref(":visited") }}</code>
{{!}}Any E element that is a hyperlink to a URL that the user ''has'' visited recently
{{!}}}                           

'''Note: '''The information that can be obtained from the :visited selector is restricted in {{ gecko("2.0") }}. See [[Privacy and the :visited selector]] for more details.

  
The {{ cssxref("cursor") }} property specifies the shape of the pointer: Some of the common shapes are as follows. Place your mouse over the items in this list to see the actual pointer shapes in your browser:

{{{!}} border="1"
{{!}}-
{{!}}'''Selector'''
{{!}}'''Selects'''
{{!}}-
{{!}}<code>pointer</code>
{{!}}Indicating a link
{{!}}-
{{!}}<code>wait</code>
{{!}}Indicating that the program cannot accept input
{{!}}-
{{!}}<code>progress</code>
{{!}}Indicating that the program is working, but can still accept input
{{!}}-
{{!}}<code>default</code>
{{!}}The default (usually an arrow)
{{!}}}                         

An {{ cssxref("outline") }} property creates an outline that is often used to indicate keyboard focus. Its values are similar to the {{ cssxref("border") }} property, except that you cannot specify individual sides.

 
Some other features of user interfaces are implemented using attributes, in the normal way. For example, an element that is disabled or read-only has the '''disabled''' attribute or the '''readonly''' attribute. Selectors can specify these attributes like any other attributes, by using square brackets: <code>{{ mediawiki.external('disabled') }}</code> or <code>{{ mediawiki.external('readonly') }}</code>.
  
Button styling example 
These rules specify styles for a button that changes dynamically as the user interacts with it:
 
<pre>.green-button {
  background-color:#cec;
  color:#black;
  border:2px outset #cec;
  }

.green-button[disabled] {
  background-color:#cdc;
  color:#777;
  }

.green-button:active {
  border-style: inset;
}</pre>
  
This wiki does not support a user interface on the page, so these buttons do not "click". Here are some static images to illustrate the idea:

{{{!}} border="1"
{{!}}-
{{!}}                 
{{{!}} border="1"
{{!}}-
{{!}}Click Me
{{!}}Click Me
{{!}}Click Me
{{!}}-
{{!}} 
{{!}}-
{{!}}disabled
{{!}}normal
{{!}}active
{{!}}} 
{{!}}}  
       
A fully functional button also has a dark outline around the entire button when it is the default, and a dotted outline on the face of the button when it has keyboard focus. It might also have a hover effect when the pointer is over it.
   
More details 
For more information about user interfaces in CSS, see [[User interface]] in the CSS Specification.

There is an example of Mozilla's markup language for user interfaces, XUL, in Part II of this tutorial.
  
== Action: Printing a document ==

<ol>
<li>
<p>Make a new HTML document, <code>doc4.html</code>. Copy and paste the content from here:</p>

<pre>&lt;!DOCTYPE html&gt;
 &lt;html&gt;
   &lt;head&gt;
     &lt;title&gt;Print sample&lt;/title&gt;
     &lt;link rel="stylesheet" href="style4.css"&gt;
   &lt;/head&gt;
   &lt;body&gt;
     &lt;h1&gt;Section A&lt;/h11&gt;
     &lt;p&gt;This is the first section...&lt;/p&gt;
     &lt;h1&gt;Section B&lt;/h1&gt;
     &lt;p&gt;This is the second section...&lt;/p&gt;
     &lt;div id="print-head"&gt;
       Heading for paged media
     &lt;/div&gt;
     &lt;div id="print-foot"&gt;
       Page: 
     &lt;/div&gt;
 &lt;/body&gt;
 &lt;/html&gt;</pre>
</li>
<li>
<p>Make a new stylesheet, <code>style4.css</code>. Copy and paste the content from here:</p>
 
<pre>/*** Print sample ***/
 
 /* defaults  for screen */
 #print-head,
 #print-foot {
   display: none;
   }
 
 /* print only */
 @media print {
 
 h1 {
   page-break-before: always;
   padding-top: 2em;
   }
 
 h1:first-child {
   page-break-before: avoid;
   counter-reset: page;
   }
 
 #print-head {
   display: block;
   position: fixed;
   top: 0pt;
   left:0pt;
   right: 0pt;
 
   font-size: 200%;
   text-align: center;
   }
 
 #print-foot {
   display: block;
   position: fixed;
   bottom: 0pt;
   right: 0pt;
 
   font-size: 200%;
   }
 
 #print-foot:after {
   content: counter(page);
   counter-increment: page;
   }
 
 } /* end print only */</pre>
</li>
<li>
<p>View this document in your browser; it uses your browser's default style.</p>
</li>
<li>
<p>Print (or print preview) the document; the stylesheet places each section on a separate page, and it adds a header and footer to each page. If your browser supports counters, it adds a page number in the footer.</p>
<p class="note">Add screenshot of result?</p>
 
</li>
</ol>        

== Extra Challenges ==

<ol>
<li>
<p>Move the print-specific style rules to a separate CSS file.</p>
</li>
<li>
<p>Read the [@import] reference page to find details of how to import the new print-specific CSS file into your <code>style4.css</code> stylesheet.</p>
</li>
 <li>
<p>Make the headings turn blue when the mouse pointer is over them.</p>
</li>
</ol>
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}