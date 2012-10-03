{{Page_Title|Using specific list styles}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article shows the basics of using list-specific CSS to control things like bullet appearance.}}
{{Tutorial
|Content===Information: Lists==

If you took the challenge on the [/en-US/docs/CSS/Getting_Started/Content last section], then you saw how you can add content before any element to display it like a list item.

CSS provides special properties that are designed for lists. It is usually more convenient to use these properties whenever you can.

To specify the style for a list, use the [list-style] property to specify the type of marker.

The selector in your CSS rule can either select the list item elements (for example, [li], or it can select the parent list element (for example, [ul] so that the list elements inherit the style.

===Unordered lists===

In an ''unordered'' list, each list item is marked in the same way.

CSS has three types of markers, and here is how your browser displays them:

* <code>disc</code>
* <code>circle</code>
* <code>square</code>

Alternatively, you can specify the URL of an image.

These rules specify different markers for different classes of list item:

<syntaxhighlight lang="css">li.open {list-style: circle;}
li.closed {list-style: disc;}</syntaxhighlight>

When these classes are used in a list, they distinguish between open and closed items (for example, in a to-do list):

<syntaxhighlight lang="html5">
 <ul>
   <li class="open">Lorem ipsum</li>
   <li class="closed">Dolor sit</li>
   <li class="closed">Amet consectetuer</li>
   <li class="open">Magna aliquot</li>
   <li class="closed">Autem vellum</li>
 </ul>
</syntaxhighlight>

The result might look like:

<p class="note">Add screenshot of results? Or dabblet?</p>

===Ordered lists===

In an ''ordered'' list, each list item is marked differently to show its position in the sequence.

Use the [list-style] property to specify the type of marker:

* <code>decimal</code>
* <code>lower-roman</code>
* <code>upper-roman</code>
* <code>lower-latin</code>
* <code>upper-latin</code>

<p class="note">Add screenshot of results? Or dabblet?</p>

This rule specifies that in [ol] elements with the class <code>info</code>, the items are identified with capital letters.

<pre> ol.info {list-style: upper-latin;}</pre>

The [li] elements in the list inherit this style:</nowiki>

<p class="note">Add screenshot of result? Or dabblet?</p>

The {{ cssxref("list-style") }} property is a shorthand property. In complex stylesheets you might prefer to use separate properties to set separate values. For links to these separate properties, and more details of how CSS specifies lists, see the {{ cssxref("list-style") }} reference page.

If you are using a markup language like HTML that provides conventional tags for unordered ({{ HTMLElement("ul") }}) and ordered ({{ HTMLElement("ol") }}) lists, then it is good practice to use the tags in the way they were intended. However, you can use CSS to make {{ HTMLElement("ul") }} display ordered and {{ HTMLElement("ol") }} display unordered if you wish.

Browsers differ in the way they implement the styles for lists. Do not expect your stylesheet to give identical results in all browsers.

===Counters===

'''Note: ''' Some browsers do not support counters. The [http://www.quirksmode.org/css/contents.html CSS contents and browser compatibility] page on the [http://www.quirksmode.org/ Quirks Mode site] contains a detailed chart of browser compatibility for this and other CSS features. Individual pages in the [/en/CSS_Reference CSS Reference] on this site also have browser compatibility tables.

You can use counters to number any elements, not only list items. For example, in some documents you might want to number headings or paragraphs.

To specify numbering, you need a ''counter'' with a name that you specify.

In some element before the counting is to start, reset the counter with the property {{ cssxref("counter-reset") }} and the name of your counter. The parent of the elements you are counting is a good place to do this, but you can use any element that comes before the list items.

In each element where the counter increments, use the property {{ cssxref("counter-increment") }} and the name of your counter.

To display your counter, add {{ cssxref(":before") }} or {{ cssxref(":after") }} to the selector and use the <code>content</code> property (as you did on the previous page, '''[/en/CSS/Getting_Started/Content Content]''').

In the value of the <code>content</code> property, specify <code>counter()</code> with the name of your counter. Optionally specify a type. The types are the same as in the '''Ordered lists''' section above.

Normally the element that displays the counter also increments it.

<syntaxhighlight lang="css">h3.numbered {counter-reset: mynum;}</syntaxhighlight>

This rule displays and increments the counter for every {{ HTMLELement("p") }} element with the class <code>numbered</code><nowiki>:</nowiki>

 
<syntaxhighlight lang="css">p.numbered:before {
   content: counter(mynum) ": ";
   counter-increment: mynum;
   font-weight: bold;
}</syntaxhighlight>

The result looks like this:

<p class="note">Add screenshot of result? Or dabblet?</p>

You cannot use counters unless you know that everyone who reads your document has a browser that supports them.

If you are able to use counters, they have the advantage that you can style the counters separately from the list items. In the example above, the counters are bold but the list items are not.

You can also use counters in more complex ways—for example, to number sections, headings, subheadings and paragraphs in formal documents. For details, see [http://www.w3.org/TR/CSS21/generate.html#counters Automatic counters and numbering] in the CSS Specification.

==Action: Styled lists==

<ol>
<li><p>Make a new HTML document, <code>doc2.html</code>. Copy and paste the content from here:</p>

<syntaxhighlight lang="html5"> <!DOCTYPE html>
 <html>
   <head>
     <meta charset="UTF-8">
     <title>Sample document 2</title>
     <link rel="stylesheet" href="style2.css">
   </head>
   <body>
  
     <h3 id="oceans">The oceans</h3>
     <ul>
       <li>Arctic</li>
       <li>Atlantic</li>
       <li>Pacific</li>
       <li>Indian</li>
       <li>Southern</li>
     </ul>
  
     <h3 class="numbered">Numbered paragraphs</h3>
     <p class="numbered">Lorem ipsum</p>
     <p class="numbered">Dolor sit</p>
     <p class="numbered">Amet consectetuer</p>
     <p class="numbered">Magna aliquot</p>
     <p class="numbered">Autem vellum</p>
  
   </body>
 </html></syntaxhighlight></li>

<li><p>Make a new stylesheet, <code>style2.css</code>. Copy and paste the content from here:</p>

<syntaxhighlight lang="css">/* numbered paragraphs */
 h3.numbered {counter-reset: mynum;}
  
 p.numbered:before {
   content: counter(mynum) ": ";
   counter-increment: mynum;
   font-weight: bold;
 }</syntaxhighlight>

<p>If the layout and comment are not to your taste, change them.</p>
</li>
<li>
<p>Open the document in your browser. If your browser supports counters, you see something like the example below. If your browser does not support counters, then you do not see the numbers (and probably not even the colons):</p>

<p class="note">Add screenshot of result? Or dabblet?</p>
</li>
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Exercise questions===

* Add a rule to your stylesheet, to number the oceans using Roman numerals from i to v:
* Change your stylesheet to identify the headings with capital letters in parentheses like this:
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Lists
|MSDN_link=
|HTML5Rocks_link=
}}