---
title: 'Using specific list styles'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Lists)'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
summary: 'This article shows the basics of using list-specific CSS to control things like bullet appearance.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/using specific list styles'

---
<p><br/></p>
<h2>Summary</h2>
<p>
This article shows the basics of using list-specific CSS to control things like bullet appearance.</p>
<h2>Information: Lists</h2>
<p>You may recall from previous articles that you can add content before any element to display it as a list item. However, 
CSS provides special properties that are designed for lists, and it is usually more convenient to use these properties whenever you can.
</p><p>To specify the style for a list, use the <a href="/css/properties/list-style">list-style</a> property to specify the type of marker. 
The selector in your CSS rule can either select the list item elements <code>li</code>, or it can select the parent list element <code>ul</code> so that its list elements inherit the style.
</p>
<h3>Unordered lists</h3>
<p>In an <i>unordered</i> list, each list item is marked in the same way. CSS has three types of bullet markers: <code>disc</code>, <code>circle</code>,
and <code>square</code>.
Alternatively, you can specify the URL of an image file for the bullet icon.
</p><p>These rules specify different markers for different classes of list items:
</p><p><br/></p>
<pre class="css">
li.open {list-style: circle;}
li.closed {list-style: disc;}

</pre>
<p><br/>
When these classes are used in a list, they distinguish between open and closed items (for example, in a to-do list):
</p><p><br/></p>
<pre class="html">
 &lt;ul&gt;
   &lt;li class="open"&gt;Lorem ipsum&lt;/li&gt;
   &lt;li class="closed"&gt;Dolor sit&lt;/li&gt;
   &lt;li class="closed"&gt;Amet consectetuer&lt;/li&gt;
   &lt;li class="open"&gt;Magna aliquot&lt;/li&gt;
   &lt;li class="closed"&gt;Autem vellum&lt;/li&gt;
 &lt;/ul&gt;

</pre>
<p><br/>
The result might look like this:
</p><p>
<img alt="csslists1.png" src="//static.webplatform.org/e/e1/csslists1.png" width="195" height="113"/></p><p><i>Figure 1. Open and closed (circle and disc) list item bullets.</i>
</p><p>You can also use <a href="/css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-child.28.29_pseudo-class">:nth-child</a> pseudo-class with the same result.
</p>
<h3>Ordered lists</h3>
<p>In an <i>ordered</i> list, each list item is marked differently to show its position in the sequence.
</p><p>Again, use the <a href="/css/properties/list-style">list-style</a> property to specify the type of marker: <code>decimal</code>, 
<code>lower-roman</code>, <code>upper-roman</code>, <code>lower-latin</code>, or <code>upper-latin</code>.
</p><p>This rule specifies that in <code>ol</code> elements with the class <code>info</code>, the items are identified with capital letters.
</p><p><br/></p>
<pre class="css">
ol.info {list-style: upper-latin;}

</pre>
<p><br/>
The <code>li</code> elements in the list inherit this style:
</p><p><br/></p>
<pre class="html">
&lt;ol class="info"&gt;
   &lt;li&gt;Lorem ipsum&lt;/li&gt;
   &lt;li&gt;Dolor sit&lt;/li&gt;
   &lt;li&gt;Amet consectetuer&lt;/li&gt;
   &lt;li&gt;Magna aliquot&lt;/li&gt;
   &lt;li&gt;Autem vellum&lt;/li&gt;
 &lt;/ol&gt;

</pre>
<p><br/>
And that result might look like this:
</p><p>
<img alt="csslists2.png" src="//static.webplatform.org/2/2f/csslists2.png" width="202" height="116"/></p><p><i>Figure 2. Ordered list items marked with capital letters.</i>
</p><p>The <code>list-style</code> property is a shorthand property. In complex style sheets, you might prefer to use separate properties to set separate values. For links to these separate properties, and to learn more details about how CSS specifies lists, see <a href="/css/properties/list-style">list-style</a>.
</p><p>Browsers differ in the way they implement the styles for lists. Do not expect your style sheet to provide identical results in all browsers.
</p>
<h3>Counters</h3>
<p><b>Note: </b> Some browsers do not support counters. The <a rel="nofollow" class="external text" href="http://www.quirksmode.org/css/contents.html">CSS contents and browser compatibility</a> page on the <a rel="nofollow" class="external text" href="http://www.quirksmode.org/">Quirks Mode</a> site contains a detailed chart of browser compatibility for this and other CSS features. You can also find useful information about browser compatibility at the extensive <a rel="nofollow" class="external text" href="http://caniuse.com">Can I Use</a> site.
</p><p>You can use counters to number any elements, not just list items. For example, in some documents you might want to number headings or paragraphs.
</p><p>To specify numbering, you can add a <i>counter</i> with a name that you specify.
</p><p>In some element before the counting is to start, reset the counter with the property <code>counter-reset</code> and the name of your counter. The parent of the elements you are counting is a good place to do this, but you can use any element that comes before the list items.
</p><p>In each element where the counter should increment, use the property <code>counter-increment</code> and the name of your counter.
Normally the element that displays the counter also increments it.
</p><p>To display your counter, add <code>:before</code> or <code>:after</code> to the selector and use the <code>content</code> property to position the counter with the element. 
In the value of the <code>content</code> property, specify <code>counter()</code> with the name of your counter. Optionally specify a type. The types are the same as in the <b>Ordered lists</b> section above.
</p><p>For example, this rule resets a counter called "mynum" when an <code>h3</code> with a class of <code>numbered</code> is encountered, preparing the paragraphs following the <code>h3</code> to be numbered.
</p><p><br/></p>
<pre class="css">
h3.numbered {counter-reset: mynum;}

</pre>
<p><br/>
This rule displays and increments the counter for every subsequent <code>p</code> element with the class <code>numbered</code>.
</p><p><br/></p>
<pre class="css">
p.numbered:before {
   content: counter(mynum) ": ";
   counter-increment: mynum;
   font-weight: bold;
}

</pre>
<p><br/>
So, for this HTML:
</p><p><br/></p>
<pre class="html">
&lt;h3 class="numbered"&gt;This is an H3&lt;/h3&gt;
&lt;p class="numbered"&gt;This is a paragraph.&lt;/p&gt;
&lt;p class="numbered"&gt;This is a paragraph.&lt;/p&gt;
&lt;p class="numbered"&gt;This is a paragraph.&lt;/p&gt;

</pre>
<p><br/>
the result looks like this:
</p><p>
<img alt="csslists3.png" src="//static.webplatform.org/a/a0/csslists3.png" width="203" height="140"/></p><p><i>Figure 3. Numbered paragraphs using the <code>counter</code> property.</i>
</p><p>You cannot use counters unless you are sure that everyone who reads your document has a browser that supports them.
If you are able to use counters, they have the advantage that you can style the counters separately from the list items. In the example above, the counters are bold but the list items are not.
</p><p>You can also use counters in more complex ways—for example, to number sections, headings, subheadings and paragraphs in formal documents. For details, see <a rel="nofollow" class="external text" href="http://www.w3.org/TR/CSS21/generate.html#counters">Automatic counters and numbering</a> in the CSS Specification.
</p>
<h2>Action: Styled lists</h2>
<ol><li><p>Make a new HTML document, and name it <code>doc2.html</code>. Copy the code below and paste it into the document:</p>
<p><br/></p>
<pre class="html">
 &lt;!DOCTYPE html&gt;
 &lt;html&gt;
   &lt;head&gt;
     &lt;meta charset="UTF-8"&gt;
     &lt;title&gt;Sample document 2&lt;/title&gt;
     &lt;link rel="stylesheet" href="style2.css"&gt;
   &lt;/head&gt;
   &lt;body&gt;
  
     &lt;h3 id="oceans"&gt;The oceans&lt;/h3&gt;
     &lt;ul&gt;
       &lt;li&gt;Arctic&lt;/li&gt;
       &lt;li&gt;Atlantic&lt;/li&gt;
       &lt;li&gt;Pacific&lt;/li&gt;
       &lt;li&gt;Indian&lt;/li&gt;
       &lt;li&gt;Southern&lt;/li&gt;
     &lt;/ul&gt;
  
     &lt;h3 class="numbered"&gt;Numbered paragraphs&lt;/h3&gt;
     &lt;p class="numbered"&gt;Lorem ipsum&lt;/p&gt;
     &lt;p class="numbered"&gt;Dolor sit&lt;/p&gt;
     &lt;p class="numbered"&gt;Amet consectetuer&lt;/p&gt;
     &lt;p class="numbered"&gt;Magna aliquot&lt;/p&gt;
     &lt;p class="numbered"&gt;Autem vellum&lt;/p&gt;
  
   &lt;/body&gt;
 &lt;/html&gt;

</pre>
</li>
<li><p>Make a new style sheet, and name it <code>style2.css</code>. Copy the CSS below and paste it into the style sheet:</p>
<pre class="css">
/* numbered paragraphs */
 h3.numbered {counter-reset: mynum;}
  
 p.numbered:before {
   content: counter(mynum) ": ";
   counter-increment: mynum;
   font-weight: bold;
 }

</pre>
<p><br/></p>
<p>If desired, you can edit the layout and comments.</p>
</li>
<li>
<p>Open the document in your browser. If your browser supports counters, you see something like the example below. If your browser does not support counters, then you will not see the numbers (and it is likely that even the colons will not display):</p>
<p>
<img alt="csslists4.png" src="//static.webplatform.org/7/78/csslists4.png" width="262" height="365"/></p><p><i>Figure 4. Unordered list items and numbered paragraphs.</i>
</p>
</li>
<p>It is also important to mention for this tutorial that styled lists are often used as menus because of semantics. For that people use css properties like list-style: none, display: inline-block or block etc, pseudo-classes like ::before and ::after and other custom styles for these items to look beautiful.
</p><p><br/></p><p><br/></p>
<h2>See also</h2>
<h3>Exercise questions</h3>
</ol><ul><li> Add a rule to your stylesheet to number the oceans using Roman numerals from i to v:</li>
<li> Change your stylesheet to identify the headings with capital letters in parentheses.</li></ul>
