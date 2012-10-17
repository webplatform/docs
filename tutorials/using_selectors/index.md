{{Page_Title|Using selectors}}
{{Flags}}
{{Byline}}
{{Summary_Section|This guide looks at CSS selectors — the mechanism you use to select which element receives styles — in detail, the different types of selector available, and how different kinds of selectors have different priorities.}}
{{Tutorial
|Content=== Information: Selectors ==
 
CSS has its own terminology to describe the CSS language. Previously in this tutorial, you created a line in your stylesheet like this:
 
<syntaxhighlight lang="css">strong {
  color: red;
}</syntaxhighlight>
 
In CSS terminology, this entire line is a ''rule''. This rule starts with <code>strong</code>, which is a ''selector''. It selects which elements in the DOM the rule applies to.
  
* The part inside the curly braces is the ''declaration''. 
* The keyword <code>color</code> is a ''property'', and <code>red</code> is a ''value''.
* The semicolon after the property-value pair separates it from other property-value pairs in the same declaration.

This guide refers to a selector like <code>strong</code> as a ''tag'' selector, and you'll also see it commonly referred to as an ''element'' selector. The CSS Specification refers to it as a ''type'' selector.
 
In addition to tag names, you can use attribute values in selectors. This allows your rules to be more specific. Two attributes have special status for CSS. They are [[class]] and [[id]].

=== Class selectors ===
 
Use the [[class]] attribute in an element to assign the element to a named class. It is up to you what name you choose for the class. Multiple elements in a document can have the same class value.
 
In your stylesheet, type a full stop (period) before the class name when you use it in a selector.
 
=== ID selectors ===
 
Use the [[id]] attribute in an element to assign an ID to the element. It is up to you what name you choose for the ID. The ID name must be unique in the document.
 
In your stylesheet, type a number sign (hash) before the ID when you use it in a selector.
  
===Class and ID selector example===

This HTML tag has both a <code>class</code> attribute and an <code>id</code> attribute:
  
<syntaxhighlight lang="html5"><p class="key" id="principal"></syntaxhighlight>
 
The '''id''' value, <code>principal</code>, must be unique in the document, but other tags in the document can have the same '''class''' name, <code>key</code>.
 
In a CSS stylesheet, this rule makes all the elements with class <code>key</code> green. (They might not all be {{ HTMLElement("p") }} elements.)
 
<syntaxhighlight lang="css">.key {
  colour: green;
}</syntaxhighlight>
 
This rule makes the one element with the '''id''' <code>principal</code> bold:
 
<syntaxhighlight lang="css">#principal {
  font-weight: bolder;
}</syntaxhighlight>
  
If more than one rule applies to an element and specifies the same property, then CSS gives priority to the rule that has the more specific selector. An ID selector is more specific than a class selector, which in turn is more specific than a tag selector.
  
===Combining selectors===
You can also combine selectors, making a more specific selector.

For example, the selector <code>.key</code> selects all elements that have the class name <code>key</code>. The selector <code>p.key</code> selects only {{ HTMLElement("p") }} elements that have the class name <code>key</code>.
 
You are not restricted to the two special attributes, <code>class</code> and <code>id</code>. You can specify other attributes by using square brackets. For example, the selector <code>[type='button']</code> selects all elements that have a <code>type</code> attribute with the value <code>button</code>.
  
If the stylesheet has conflicting rules and they are equally specific, then CSS gives priority to the rule that is later in the stylesheet.
 
When you have a problem with conflicting rules, try to resolve it by making one of the rules more specific, so that it has priority. If you cannot do that, try moving one of the rules nearer the end of the stylesheet so that it has priority.
 
=== Pseudo-class selectors ===
 
A CSS [[pseudo-class]] is a keyword added to selectors that specifies a special state of the element to be selected. For example {{ Cssxref(":hover") }} will apply a style when the user hovers over the element specified by the selector.

 
Pseudo-classes, together with pseudo-elements, let you apply a style to an element not only in relation to the content of the document tree, but also in relation to external factors like the history of the navigator ({{ cssxref(":visited") }}, for example), the status of its content (like {{ cssxref(":checked") }} on some form elements), or the position of the mouse (like {{ cssxref(":hover") }} which lets you know if the mouse is over an element or not). To see a complete list of selectors, visit [[CSS3 Selectors working spec]].
 
<syntaxhighlight lang="css">selector:pseudo-class {
  property: value;
} </syntaxhighlight>
  
==== List of pseudo-classes ====
 
* {{ Cssxref(":link") }}
* {{ Cssxref(":visited") }}
* {{ Cssxref(":active") }}
* {{ Cssxref(":hover") }}
* {{ Cssxref(":focus") }}
* {{ Cssxref(":first-child") }}
* {{ Cssxref(":nth-child") }}
* {{ Cssxref(":nth-last-child") }}
* {{ Cssxref(":nth-of-type") }}
* {{ Cssxref(":first-of-type") }}
* {{ Cssxref(":last-of-type") }}
* {{ Cssxref(":empty") }}
* {{ Cssxref(":target") }}
* {{ Cssxref(":checked") }}
* {{ Cssxref(":enabled") }}
* {{ Cssxref(":disabled") }}
 
== Information: Selectors based on relationships ==
 
CSS has some ways to select elements based on the relationships between elements. You can use these to make selectors that are more specific.
                         
{{{!}} border="1"
{{!}}+ Common selectors based on relationships
{{!}}-
{{!}}'''Selector'''
{{!}}'''Selects'''
{{!}}-
{{!}}<code>A E</code>
{{!}}Any E element that is a ''descendant'' of an A element (that is: a child, or a child of a child, ''etc''.)
{{!}}-
{{!}}<code>A > E</code>
{{!}}Any E element that is a child of an A element
{{!}}-
{{!}}<code>E:first-child</code>
{{!}}Any E element that is the first child of its parent
{{!}}-
{{!}}<code>B + E</code>
{{!}}Any E element that is the next ''sibling'' of a B element (that is: the next child of the same parent)
{{!}}} 

You can combine these to express complex relationships.

 You can also use the symbol <code>*</code> (asterisk) to mean "any element".
 
====Example of selectors based on relationships====

An HTML table has an <code>id</code> attribute, but its rows and cells do not have individual identifiers:
 
<syntaxhighlight lang="html5"><table id="data-table-1">
…
<tr>
<td>Prefix</td>
<td>0001</td>
<td>default</td>
</tr>
…</syntaxhighlight>
 
These rules make the first cell in each row bold, and the second cell in each row monospaced. They only affect one specific table in the document:
 
<syntaxhighlight lang="css">data-table-1 td:first-child {font-weight: bolder;}
data-table-1 td:first-child + td {font-family: monospace;}</syntaxhighlight>
 
The result looks like:
       
{{{!}} border="1"
{{!}}-
{{!}}         
{{{!}} border="1"
{{!}}-
{{!}}'''Prefix'''
{{!}}<code>0001</code>
{{!}}default
{{!}}} 
{{!}}}   

===Increasing specificity===
  
In the usual way, if you make a selector more specific, then you increase its priority.
 
If you use these techniques, you avoid the need to specify <code>class</code> or <code>id</code> attributes on so many tags in your document. Instead, CSS does the work.
 
In large designs where speed is important, you can make your stylesheets more efficient by avoiding complex rules that depend on relationships between elements.
 
For more examples about tables, see [[Tables]] in the CSS Reference page.

== Action: Using class and ID selectors ==
 
<ol>
<li><p>Edit your HTML file, and duplicate the paragraph by copying and pasting it.</p></li>
<li><p>Then add '''id''' and '''class''' attributes to the first copy, and an '''id''' attribute to the second copy as shown below. Alternatively, copy and paste the entire file again:</p>

<syntaxhighlight lang="html5"><!doctype html>
 <html>
   <head>
   <meta charset="UTF-8">
   <title>Sample document</title>
   <link rel="stylesheet" href="style1.css">
   </head>
   <body>
     <p id="first">
       <strong class="carrot">C</strong>ascending
       <strong class="spinach">S</strong>tyle
       <strong class="spinach">S</strong>heets
     </p>
     <p id="second">
           <strong>C</strong>ascending
           <strong>S</strong>tyle
           <strong>S</strong>heets
         </p>
   </body>
 </html></syntaxhighlight>
</li>
<li><p>Now edit your CSS file. Replace the entire contents with:</p>

<syntaxhighlight lang="css">strong { color: red; }
 .carrot { color: orange; }
 .spinach { color: green; }
 #first { font-style: italic; }</syntaxhighlight>
</li>
<li><p>Save the files and refresh your browser to see the result:</p>

</li>
</ol>

[[File:usingclassandid_result.jpg]]

You can try rearranging the lines in your CSS file to show that the order has no effect. The class selectors <code>.carrot</code> and <code>.spinach</code> have priority over the tag selector <code>strong</code>.   The ID selector <code>#first</code> has priority over the class and tag selectors.
  
=== Exercise questions === 

* Without changing your HTML file, add a single rule to your CSS file that keeps all the initial letters that same colour as they are now, but makes all the other text in the second paragraph blue:
* Now change the rule you have just added (without changing anything else), to make the first paragraph blue too:

== Action: Using pseudo-classes selectors ==
 
<ol>
<li><p>Create an HTML like the following:</p>

<syntaxhighlight lang="html5"><!doctype html>
 <html>
   <head>
   <meta charset="UTF-8">
   <title>Sample document</title>
   <link rel="stylesheet" href="style1.css">
   </head>
   <body>
     <p>Go to our <a class="homepage" href="http://www.example.com/" title="Home page">Home page</a>.</p>
   </body>
 </html></syntaxhighlight></li>
 
<li><p>Now edit your CSS file. Replace the entire contents with:</p>

<syntaxhighlight lang="css">a.homepage:link, a.homepage:visited {
   padding: 1px 10px 1px 10px;
   color: #fff;
   background: #666;
   border-radius: 3px;
   border: 1px outset rgba(50,50,50,.5);
   font-family: georgia, serif;
   font-size: 14px;
   font-style: italic;
   text-decoration: none;
 }
 
 a.homepage:hover, a.homepage:focus, a.homepage:active {
   background-color: #333;
 }</syntaxhighlight>
</li> 
<li><p>Save the files and refresh your browser to see the result (put the mouse over the following link to see the effect):</p>
[[File:pseudoclassselector_result.jpg]]
<p>The link turns to dark grey.</p></li>
</ol> 

== Action: Using selectors based on relationships and pseudo-classes ==
 
With selectors based on relationships and pseudo-classes you can create complex cascade algorithms. This is a common technique used, for example, in order to create '''pure-CSS drop down menus''' (that is only CSS, without using [[javascript|JavaScript]]). The essence of this technique is the creation of a rule like the following:
 
<syntaxhighlight lang="css">div.menu-bar ul ul {
  display: none;
}

div.menu-bar li:hover > ul {
  display: block;
}</syntaxhighlight>
 
to be applied to an HTML structure like the following:

<syntaxhighlight lang="html5"><div class="menu-bar">
  <ul>
    <li>
      <a href="example.html">Menu</a>
      <ul>
        <li>
          <a href="example.html">Link</a>
        </li>
        <li>
          <a class="menu-nav" href="example.html">Submenu</a>
          <ul>
            <li>
              <a class="menu-nav" href="example.html">Submenu</a>
              <ul>
                <li><a href="example.html">Link</a></li>
                <li><a href="example.html">Link</a></li>
                <li><a href="example.html">Link</a></li>
                <li><a href="example.html">Link</a></li>
              </ul>
            </li>
            <li><a href="example.html">Link</a></li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</div></syntaxhighlight>
 
See our complete [[CSS-based drop down menu example]] for a possible cue.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Selectors
|MSDN_link=
|HTML5Rocks_link=
}}