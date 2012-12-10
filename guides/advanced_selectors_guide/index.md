{{Page_Title|Advanced selectors guide}}
{{Flags}}
{{Byline}}
{{Summary_Section|This guide gives a detailed explanation of most of the advanced CSS selectors available.}}
{{Guide
|Content=== Introduction ==
 
In our [http://docs.webplatform.org/wiki/tutorials/CSS_basics CSS basics] article, we introduced the most basic of CSS selectors: element, class, and id selectors. With these selectors you can accomplish a lot, but this certainly is not an exhaustive list of selectors — there are other selectors that allow you to select elements to style based on more specific criteria. In this article, most of the advanced CSS selectors are described.

Note: This article discusses "most" of the advanced selectors, because although most modern browsers support all the selectors listed in the [http://www.w3.org/TR/selectors/ CSS3 selectors module], new selectors are being added and modified all the time--keep checking the [http://www.w3.org/TR/selectors4/ CSS4 selectors draft] for updates. New selectors will be added to this article as they receive more widespread browser support.
 
You will see many of these selectors used throughout our articles as you read on. Don't worry if you don't understand them all immediately: keep referencing this article as needed. 
 
== Universal selectors ==
 
Universal selectors select every element on a page. For example, the following rule says that every element on the page will display a solid 1 pixel black border:
 
<syntaxhighlight lang="css">* {
  border: 1px solid #000000;
}</syntaxhighlight>
 
== Attribute selectors ==
 
Attribute selectors allow you to select elements based on the attributes they contain. For example, you can select every <code>&lt;img&gt;</code> element with an <code>alt</code> attribute using the following selector:
 
<syntaxhighlight lang="css">img[alt] {
  border: 1px solid #000000;
}</syntaxhighlight>
 
Note the square brackets in the example above.
 
Using the above selector, you could perhaps add a black border around any images that have an <code>alt</code> attribute, and style other images with a bright red border —  this is a useful technique for accessibility testing.

=== Selecting by attribute value ===
 
Attribute selectors instantly become more useful when you consider that you can select by ''attribute value'', not just an attribute's name. The following rule selects all images with an <code>src</code> attribute value of <code>alert.gif</code>:
 
<syntaxhighlight lang="css">img[src="alert.gif"] {
  border: 1px solid #000000;
}</syntaxhighlight>
 
Again this style is useful for debugging purposes. You can also use it to style important icons or links without requiring additional classes and IDs.

Note that this code is not supported by IE6 and below.

=== Selecting based on substrings within the attribute value ===

This is where attribute selectors become even more useful. To begin, you can select and style our <code>&lt;img src="alert.gif"&gt;</code> element using the following rule:

<syntaxhighlight lang="css">img[src^="alert"] {
  border: 1px solid #000000;
}</syntaxhighlight>

The ^ character dictates that this selector affects <code>&lt;img&gt;</code> elements only if they contain the string <code>alert</code> at the start of the <code>src</code> attribute value.

You can also select a <code>&lt;img src="alert.gif"&gt;</code> element using this rule:

<syntaxhighlight lang="css">img[src$="gif"] {
  border: 1px solid #000000;
}</syntaxhighlight>

The $ character dictates that this selector should select <code>&lt;img&gt;</code> elements only if they contain the string <code>gif</code> at the end of the <code>src</code> attribute value. This is really useful for styling links that point to specific types of resources, such as PDF files or word documents. 

And finally, you can select a <code>&lt;img src="alert.gif"&gt;</code> element like this:

<syntaxhighlight lang="css">img[src*="ert"] {
  border: 1px solid #000000;
}</syntaxhighlight>

The * character dictates that this selector should affect <code>&lt;img&gt;</code> elements only if they have the string <code>ert</code> anywhere within the <code>src</code> attribute value.

Note: These advanced selectors are not supported by IE8 and below.

=== Selecting based on delimited items within the attribute value ===

If you have an element on a page with a number of classes applied to it, for example:

<pre>&lt;article class="featured archive english"&gt;&lt;/article&gt;</pre>

You could select it using any of the following selectors:

<syntaxhighlight lang="css">article[class~="featured"]
article[class~="archive"]
article[class~="english"]</syntaxhighlight>

The ~ character dictates that these selectors should select an <code>&lt;article&gt;</code> element whose <code>class</code> attribute value is a list of whitespace-separated values, but only if one of those values is the value given inside the quotes. 

Next, take a look at an element on a page with an ID value in the form of hyphen-separated list:

<pre>&lt;article id="english-daily-feature"&gt;&lt;/article&gt;</pre>

You can select it using the following selector:

<syntaxhighlight lang="css">article[id|="english"]</syntaxhighlight>

The {{!}} character dictates that this selector should select an <code>&lt;article&gt;</code> element whose <code>id</code> attribute value is a list of hyphen-separated values, but only if the leftmost value is <code>english</code>. 

Note: These selectors are not supported by IE8 and below.

== Child selector ==
 
You can use a child selector to select specific elements that are children of other specific elements. For example, the following rule will turn the text of <code>&lt;strong&gt;</code> elements that are children of <code>&lt;h3&gt;</code> elements blue, without affecting other <code>&lt;strong&gt;</code> elements:
 
<syntaxhighlight lang="css">h3 > strong {
  color: blue;
}</syntaxhighlight>
 
Note that child selectors are not supported in IE6 or below.

Note also that the > character is often referred to as a combinator in this context — it combines multiple elements together in one selector.
 
== Descendent selector ==
 
Descendent selectors are similar to child selectors, except that child selectors only select immediate descendants; descendent selectors select matching elements anywhere in the element hierarchy, not just direct descendants. Investigate what this means by examining the following HTML snippet:
 
<syntaxhighlight lang="html5"><div>
  <p>hello</p>
  <article> 
    <p>In this paragraph I will say goodbye</p>
  </article>
</div></syntaxhighlight>
 
In this snippet, the <code>&lt;div&gt;</code> element is the parent of all other elements. It has two children, a <code>&lt;p&gt;</code> and an <code>&lt;article&gt;</code>. The <code>&lt;article&gt;</code> element has a single child element: another <code>&lt;p&gt;</code>.

You could use a child selector to select just the <code>&lt;p&gt;</code> immediately inside the <code>&lt;div&gt;</code>, like so:
 
<syntaxhighlight lang="css">div > p {
 …
}</syntaxhighlight>
 
If you instead use a descendent selector, as follows:
 
<syntaxhighlight lang="css">div p {
 …
}</syntaxhighlight>
 
Then, both of the <code>&lt;p&gt;</code> elements are selected.
 
== Adjacent sibling selector ==
 
This selector allows you to select a specific element that comes directly after another specific element, on the same level in the element hierarchy. Review the following example:

<syntaxhighlight lang="html5"><h2>My heading</h2>
<p>My first paragraph</p>
<p>My second paragraph</p>
<p>My third paragraph</p>
<p>My fourth paragraph</p>
<p>My fifth paragraph</p></syntaxhighlight>

<p>If you wanted to select just the <code>&lt;p&gt;</code> element that comes immediately after the <code>&lt;h2&gt;</code> element (and any other such <code>&lt;p&gt;</code> elements that might appear later in the document) you could use the following rule:
 
<syntaxhighlight lang="css">h2 + p {
 ...
}</syntaxhighlight>
 
Note that the adjacent sibling selector is not supported in IE6 or below.

Note also that the + character is often referred to as a combinator in this context — it combines multiple elements together in one selector.

== General sibling selectors ==
 
The general sibling selector is very similar to the adjacent sibling selector, except that it allows you to select all siblings of the specified element type, not just the one immediate next to the element on the left side. The CSS syntax looks like this:

<syntaxhighlight lang="css">h2 ~ p {
 ...
}</syntaxhighlight>

Returning to our previous example, this ruleset would select all five paragraph elements, not just the first one. It would also select the paragraph shown below:

<syntaxhighlight lang="html5"><h2>My heading</h2>
<h3>My sub heading</h3>
<p>My paragraph</p></syntaxhighlight>
 
Note that the general sibling selector is not supported in IE8 or below.

Note also that the ~ character is often referred to as a combinator in this context — it combines multiple elements together in one selector.
 
== Pseudo-classes ==
 
Pseudo-classes are used to provide styles not for elements, but for various states of elements.

=== Link and user action pseudo-classes ===

The most common pseudo-classes you will come across are those used to style link states (they are described in full usage in [http://docs.webplatform.org/wiki/Styling_lists_and_links Styling lists and links]):
 
* <code>:link</code> — the normal, default state of links, as displayed when the page first loads in a browser.
* <code>:visited</code> — selects links that you have already visited in the browser you are currently using.
* <code>:focus</code> — selects links that currently have the text indicator (location of cursor) within them.
* <code>:hover</code> — selects links that the cursor is currently hovering over.
* <code>:active</code> — selects links that are currently being clicked.

Note that the last three listed above (called "user action pseudo-classes" — the first two are the link pseudo-classes) can be used to style the states of any element. They are often used when styling a user interface. For example, you can set a different style of a form input field when it is tabbed into, or you might want an information box to appear only when the cursor hovers over a certain area of the screen. 
 
Check out the following examples. The CSS rules below applies a link style to display blue links (which is the default link style in most browsers anyway). When hovered over, the default link underline disappears. To achieve the same effect when the link is focused via the keyboard, the <code>:hover </code> rule is duplicated with the <code>:focus </code> selector. When a link has already been visited, it turns gray. Finally, when a link is active, it is bold, as an extra clue to visitors that something significant is happening.

 
<syntaxhighlight lang="css">a:link {
 color: blue;
}

a:visited {
 color: gray;
}

a:hover, a:focus {
text-decoration: none;
}

a:active {
 font-weight: bold;
}</syntaxhighlight>
 
Take care to specify these rules in the same order as they are shown in above, because otherwise they might not work as you expect. This is due to the way specificity causes later rules in the style sheet to override earlier rules. Specificity is covered in more detail in the article titled [[Inheritance and cascade]].
 
As another example, the <code>:focus</code> pseudo-class is also useful as a usability aid in forms. For example, you can highlight the input field that has the active blinking cursor inside it with a rule like this:

 
<syntaxhighlight lang="css">input:focus  {
  border: 2px solid black;
  background color: lightgray;
}</syntaxhighlight>
 
=== The negation (not) pseudo-class ===

The negation pseudo-class can be used to explicitly apply styles to elements that '''are not''' selected by a simple selector. For example, imagine that you want to apply some styling to a number of content blocks, all except one. The blocks could look like this:   
 
<syntaxhighlight lang="html5"><section id="abstract"> ... </section>
<section id="experiment"> ... </section>
<section id="tests"> ... </section>
<section id="results"> ... </section>
<section id="conclusion"> ... </section>
<section id="references"> ... </section></syntaxhighlight>

You can apply the styling to all sections except the references, with this rule:

<syntaxhighlight lang="css">
#abstract, #experiment, #tests, #results, #conclusion {
  ...
}
</syntaxhighlight>

Or instead, you can use the negation selector, like this:

<syntaxhighlight lang="css">
section:not(#references) {
  ...
}
</syntaxhighlight>

Which is much shorter and easy to read.

Note: The negation selector is not supported by IE8 and below.

=== The language (lang) pseudo-class ===
 
The <code>:lang</code> pseudo-class selects elements whose languages have been set to the specified language using the <code>lang</code> attribute. For example, the following HTML element:
 
<syntaxhighlight lang="html5"><p lang="en-US">A paragraph of American text, gee whiz!<p></syntaxhighlight>
 
Could be selected using the following:
 
<syntaxhighlight lang="css">p:lang(en-US) {
 ...
}</syntaxhighlight>

=== The target pseudo-class ===

The target pseudo-class allows you to select an element if it is the '''target''' of the current page URL. This is really useful and allows for some cool effects, because it effectively allows you to set styles to be applied when links are clicked. For example:

<syntaxhighlight lang="html5"><a href="#target">Click me</a>

<div id="target">Woot!</div></syntaxhighlight>

This is accomplished with a simple link followed by a <code>&lt;div&gt;</code> — the link references the <code>&lt;div&gt;</code> via its ID. The current URL only targets the <code>&lt;div&gt;</code> upon the link being clicked. To style the <code>&lt;div&gt;</code> only when the link is clicked, you could use the following rule:

<syntaxhighlight lang="css">div:target {
  ...
}</syntaxhighlight>

To see a much more involved example of <code>:target</code> usage, read the article titled [http://dev.opera.com/articles/view/css3-target-based-interfaces/ CSS3 target-based interfaces] by Corey Mwamba.

=== UI element state pseudo-classes ===

These pseudo-classes are all concerned with styling advanced states of UI elements. You'll most commonly use them to style HTML form elements, particularly when some of the new features of HTML5 forms are being used, such as built in validation. (See [HTML5 form additions] for more details.)

Imagine you are styling a basic form input with a <code>valid</code> attribute for validation:

<syntaxhighlight lang="html5"><input type="text" required></syntaxhighlight>

You can style it only when the information entered into it is valid or invalid using these two rules:

<syntaxhighlight lang="css">input:valid {}</syntaxhighlight>

and 

<syntaxhighlight lang="css">input:invalid {}</syntaxhighlight>

You can also style it depending on whether it is enabled (default) or disabled (using the <code>disabled</code> attribute), using this style:

<syntaxhighlight lang="css">input:enabled {}</syntaxhighlight>

and this style:

<syntaxhighlight lang="css">input:disabled {}</syntaxhighlight>

Finally, you can style a checkbox only when checked, like this:

<syntaxhighlight lang="css">input[type="checkbox"]:checked {}</syntaxhighlight>


=== Structural pseudo-classes ===

Structural pseudo-classes are advanced selectors that enable you to target specific elements based on their position in the document hierarchy. These were introduced in CSS3, and they are built on selectors previously discussed, such as the adjacent sibling selector.

<code>:root</code> selects the root element of the document, which is usually the <code>&lt;html&gt;</code> element. For example, this rule:

<syntaxhighlight lang="css">html:root{ ... }</syntaxhighlight>

<p><code>:nth-child(n)</code> allows you to select a repeating pattern of elements inside an continuous set of like elements, such as several list items, or several paragraphs or articles next to one another. Review this example:

<syntaxhighlight lang="html5"><ul>
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
  <li>Fourth</li>  
  <li>Fifth</li>
  <li>Sixth</li>
  <li>Seventh</li>
  <li>Eighth</li>
  <li>Ninth</li>
  <li>Tenth</li>
</ul></syntaxhighlight>

<code>n</code> is set to the pattern we want to select. In this case, to select list items, use this code:

<syntaxhighlight lang="css">li:nth-child(n)</syntaxhighlight>

To select just the odd or even list items, add this rule:

<syntaxhighlight lang="css">li:nth-child(odd)
li:nth-child(even)</syntaxhighlight>

Or you can use this rule to accomplish the same result:

<syntaxhighlight lang="css">li:nth-child(2n+1)
li:nth-child(2n+0)</syntaxhighlight>

Take a look at some other formula examples:

* <code>li:nth-child(5)</code>: select the fifth adjacent list item.
* <code>li:nth-child(4n+1)</code>: select every fourth list item, and then add 1 to each result. So numbers 5 and 9.
* <code>li:nth-child(3n-2)</code>: select every third list item, and subtract 2 from each result. So numbers 1, 4 and 7.

You can also use <code>nth-last-child(n)</code>. This does the same thing as <code>nth-child(n)</code>, but it counts from the last element in the sequence, not the first element.

<code>nth-of-type(n)</code> and <code>nth-last-of-type(n)</code> accomplish almost exactly the same goals as <code>nth-child(n)</code> and <code>nth-last-child(n)</code>, but there is one important difference: the former two ignore any rogue elements interspersed with the repeated sequence of like elements because they select by type of element, not by child number. The latter selects by child number.

Here is another example:

<syntaxhighlight lang="html5"><div>
  1. <article class="abstract"> ... </article>
  2. <article class="abstract"> ... </article>
  3. <article class="abstract"> ... </article>
  4. <article class="abstract"> ... </article>
  5. <article class="abstract"> ... </article>
  6. <blockquote><p> ... </p></blockquote>
  7. <article class="abstract"> ... </article>
  8. <article class="abstract"> ... </article>
  9. <article class="abstract"> ... </article>
</div></syntaxhighlight>

In this example we've got a <code>&lt;element&gt;</code> with eight child <code>&lt;article&gt;</code> elements, and a single <code>&lt;blockquote&gt;</code> element in the middle of them: this is child number six. There are a total of nine child elements.

If you use <code>article:nth-child(2n+0)</code> as the selector, to select all the even-numbered children of the <code>&lt;div&gt;</code>, you'd select only the <code>&lt;article&gt;</code>s in positions 2, 4 and 8: the <code>&lt;blockquote&gt;</code> (position number six) is not selected because it is not an <code>&lt;article&gt;</code>.

If you use <code>article:nth-of-type(2n+0)</code> as the selector, you would select the <code>&lt;article&gt;</code>s in positions 2, 4, 7 and 9: this occurs because it selects by the type of element, not the child position. Therefore in this case, the <code>&lt;blockquote&gt;</code> is completely ignored and the even numbered <code>&lt;article&gt;</code>s are selected. Yes, two of them are odd numbered according to my original numbering scheme because in reality the <code>&lt;blockquote&gt;</code> exists and offsets their position, but <code>article:nth-of-type(2n+0)</code> ignores the <code>&lt;blockquote&gt;</code>, effectively counting positions 7 and 9 as 6 and 8. 

Next, check out the <code>:first-child</code> and <code>:last-child</code> selectors — these pseudo-classes select only the first or last instance of an element that is the first or last child element of its parent. So, considering the above example again, we could use the following to select - respectively - the first and last <code>&lt;article&gt;</code> element:

 
<syntaxhighlight lang="css">article:first-child { ... }

article:last-child { ... }</syntaxhighlight>

<code>blockquote:first-child</code> would select nothing, because the first child is not a <code>&lt;blockquote&gt;</code>.

<code>first-of-type</code> and <code>last-of-type</code> again work in a very similar way, but they select based on the type of element, not the position of child it is. So <code>article:first-of-type</code> selects exactly the same <code>&lt;article&gt;</code> element as <code>article:first-child</code>, but <code>blockquote:first-of-type</code> selects the single <code>&lt;blockquote&gt;</code> in the example, because it is the first of its type, even though it is the sixth child.

There are a few others to consider:

* <code>only-child</code>: Selects an element only if it is the only child of its parent. The selector  <code>article:only-child</code> wouldn't select anything in our example above, because there is more than one <code>&lt;article&gt;</code> child.
* <code>only-of-type</code>: Selects an element only if it is the only sibling of its type inside the parent element. So <code>blockquote:only-of-type</code> would select the <code>&lt;blockquote&gt;</code> in the above example because it is the only one of its type that exists.
* <code>empty</code>: selects an element only if it has no children whatsoever (including text nodes). For example <code>div:empty</code> would select <code>&lt;div&gt;&lt;/div&gt;</code>, but not <code>&lt;div&gt;1&lt;/div&gt;</code> or <code>&lt;div&gt;&lt;p&gt;Hi!&lt;/p&gt;&lt;/div&gt;</code>
 
== Pseudo-elements ==
 
Pseudo elements differ from pseudo-classes in that they don't select states of elements; they select parts of an element.

=== :first-letter ===

You can select the first letter inside a given element using the following rule:
 
<syntaxhighlight lang="css">p:first-letter {
  font-weight: bold;
  font-size: 300%
  background-color: red;
}</syntaxhighlight>
 
The first letter of every paragraph will now be bold, 300% bigger than the rest of the paragraph, and have a red background. This is a good start towards creating a decent drop cap effect.

=== :first-line ===
 
To make the first line of every paragraph bold, you can use the following rule:
 
<syntaxhighlight lang="css">p:first-line {
  font-weight: bold;
}</syntaxhighlight>

=== Generated content using :before and :after ===
 
You can use the <code>:before</code> and <code>:after</code> pseudo-elements to specify that content should be inserted before and after the selected element. You then specify the content that you want to insert or generate. For example, you can use the following rule to insert a decorative image after every link on the page:

<syntaxhighlight lang="css">a:after {
  content: " " url(flower.gif);
}</syntaxhighlight>
 
You can also use the <code>attr()</code> function to insert the values of attributes of the elements after the element. For example, you could insert the target of every link in your document in brackets after each one using the following:
 
<syntaxhighlight lang="css">a:after {
  content: "" "(" attr(href) ")";
}</syntaxhighlight>
 
This is a great technique to use in a print style sheet, where it is important to display the URLs in the document rather than have them hidden inside text links (which are useless on a printed page).

You can also insert incremented numerical values after repeating elements (such as bullets or paragraphs) using the <code>counter()</code> function. This is explained in much more detail in the article titled [[http://dev.opera.com/articles/view/automatic-numbering-with-css-counters/ Automatic numbering with CSS counters]] by David Storey.
 
These selectors are not supported in IE 7 or below. Also note that you should not insert important information with CSS, because that content will be unavailable to assistive technologies. It will also be unavailable if a visitor chooses not to use the style sheet. The golden rule is that CSS rules are for styling; HTML is for displaying important content.

=== CSS3 pseudo-element double colon syntax ===

Please note that the new CSS3 way of writing pseudo-elements is to use a double colon, such as <code>a::after { … }</code>, to set them apart from pseudo-classes. You may see this sometimes in CSS. CSS3 however also still allows for single colon pseudo-elements, for the sake of backwards compatibility. For the immediate future, it is recommended to continue using the single colon syntax.
|character dictates that this selector should select an <code>&lt;article&gt;</code> element whose <code>id</code> attribute value is a list of hyphen-separated values, but only if the leftmost one of those values is <code>english</code>_ 

Note that these are not supported by IE8 and below_== Child selector ==
 
You can use a child selector to select specific elements that are children of other specific elements. For example, the following rule will turn the text of <code>&lt;strong&gt;</code> elements that are children of <code>&lt;h3&gt;</code> elements blue, but no other <code>&lt;strong&gt;</code> elements:
 
<pre>h3 > strong {
  color: blue;
}</pre>
 
Note that child selectors are not supported in IE 6 or below.

Note also that the > character is often referred to as a combinator in this context — it combines multiple elements together in one selector.
 
== Descendent selector ==
 
Descendent selectors are very similar to child selectors, except that child selectors only select immediate descendents; descendent selectors select matching elements anywhere in the element hierarchy, not just direct descendents. Let's look at what this means more carefully. Consider the following HTML snippet:
 
<pre>&lt;div&gt;
  &lt;p&gt;hello&lt;/p&gt;
  &lt;article&gt; 
    &lt;p&gt;In this paragraph I will say goodbye&lt;/p&gt;.
  &lt;/article&gt;
&lt;/div&gt;</pre>
 
In this snippet, the <code>&lt;div&gt;</code> element is the parent of all other elements. It has two children, a <code>&lt;p&gt;</code> and an <code>&lt;article&gt;</code>. The <code>&lt;article&gt;</code> element has a single child element: another <code>&lt;p&gt;</code>.

You could use a child selector to select just the <code>&lt;p&gt;</code> immediately inside the <code>&lt;div&gt;</code>, like so:
 
<pre>div > p {
 ...
}</pre>
 
If you instead used a descendent selector, as follows:
 
<pre>div p {
 ...
}</pre>
 
Both of the <code>&lt;p&gt;</code> elements would be selected.
 
== Adjacent sibling selector ==
 
This selector allows you to select a specific element that comes directly after another specific element, on the same level in the element hierarchy. Take the following example:

<pre>&lt;h2&gt;My heading&lt;/h2&gt;
&lt;p&gt;My first paragraph&lt;/p&gt;
&lt;p&gt;My second paragraph&lt;/p&gt;
&lt;p&gt;My third paragraph&lt;/p&gt;
&lt;p&gt;My fourth paragraph&lt;/p&gt;
&lt;p&gt;My fifth paragraph&lt;/p&gt;</pre>

<p>If you wanted to select just the <code>&lt;p&gt;</code> element that comes immediately after the <code>&lt;h2&gt;</code> element (and any other such <code>&lt;p&gt;</code> elements that might appear later in the document) you could use the following rule:
 
<pre><code>h2 + p {
 ...
}</code></pre>
 
Note that the adjacent sibling selector is not supported in IE6 or below.

Note also that the + character is often referred to as a combinator in this context — it combines multiple elements together in one selector.

== General sibling selectors ==
 
The general sibling selector is very similar to the adjacent sibling selector, except that it allows you to select all siblings of the specified element type, not just the one immediate next to the element on the left hand side. the syntax looks like this:

<pre><code>h2 ~ p {
 ...
}</code></pre>

Returning to our previous example, this ruleset would select all five paragraph elements, not just the first one. It would also select the paragraph shown below:

<pre>&lt;h2&gt;My heading&lt;/h2&gt;
&lt;h3&gt;My sub heading&lt;/h3&gt;
&lt;p&gt;My paragraph&lt;/p&gt;</pre>
 
Note that the general sibling selector is not supported in IE8 or below.

Note also that the ~ character is often referred to as a combinator in this context — it combines multiple elements together in one selector.
 
== Pseudo-classes ==
 
Pseudo-classes are used to provide styles not for elements, but for various states of elements.

=== Link and user action pseudo-classes ===

The most common pseudo-classes you’ll come across is those used to style link states (you'll see these in full usage in [Styling lists and links]):
 
* <code>:link</code> — the normal, default state of links, just as you first found them.
* <code>:visited</code> — selects links that you have already visited in the browser you are currently using.
* <code>:focus</code> — selects links that currently have the keyboard cursor within them.
* <code>:hover</code> — selects links that are currently being hovered over by the mouse pointer.
* <code>:active</code> — selects links that are currently being clicked on.

Note that the last three of these (these are the "user action pseudo-classes" — the first two are the link pseudo-classes) can be used the style states of pretty much any element it would make sense to use them on in a user interface. For example, you might want a form input to adopt a different style when it is tabbed into, or you might want an information box to appear only when a certain part of the screen is moused over. 
 
Let's look at some examples. The following CSS rules make it so that by default, links are blue (the default in most browsers anyway). When hovered over, the default link underline disappears. We want the same effect when the link is focused via the keyboard, so we duplicate the <code>:hover </code> rule with <code>:focus </code> . When a link has already been visited, it turns grey. Finally, when a link is active, it is bolded, as an extra clue that something significant is happening.

 
<pre>a:link {
 color: blue;
}

a:visited {
 color: gray;
}

a:hover, a:focus {
text-decoration: none;
}

a:active {
 font-weight: bold;
}</pre>
 
Take care if you don't specify these rules in the same order as they are shown in above, otherwise they might not work as you expect. This is due to the way specificity causes later rules in the stylesheet to override earlier rules. You’ll learn more about specificity in [[Inheritance and cascade]].
 
As another example, the <code>:focus</code> pseudo-class is also useful as a usability aid in forms. For example, you can highlight the input field that has the active blinking cursor inside it with a rule like this:

 
<pre>input:focus  {
  border: 2px solid black;
  background color: lightgray;
}</pre>
 
=== The negation (not) pseudo-class ===

The negation pseudo-class can be used to explicitly apply styles to elements that '''are not''' selected by a simple selector. Let's say we wanted to apply some styling to a number of content blocks, all except one. The blocks could look like so:   
 
<pre>&lt;section id="abstract"&gt; ... &lt;/section&gt;
&lt;section id="experiment"&gt; ... &lt;/section&gt;
&lt;section id="tests"&gt; ... &lt;/section&gt;
&lt;section id="results"&gt; ... &lt;/section&gt;
&lt;section id="conclusion"&gt; ... &lt;/section&gt;
&lt;section id="references"&gt; ... &lt;/section&gt;</pre>

We could apply the styling to all sections except the references by doing this:

#abstract, #experiment, #tests, #results, #conclusion {
  ...
}

Or instead, we could use the negation selector, like so:

section:not(#references) {
  ...
}

Which is much shorter and simpler.

Note: The negation selector is not supported by IE8 and below.

=== The language (lang) pseudo-class ===
 
The <code>:lang</code> pseudo-class selects elements whose languages have been set to the specified language using the <code>lang</code> attribute. For example, the following element:
 
<pre>&lt;p lang="en-US"&gt;A paragraph of American text, gee whiz!&lt;p&gt;</pre>
 
Could be selected using the following:
 
<pre>p:lang(en-US) {
 ...
}</pre>

=== The target pseudo-class ===

The target pseudo-class allows you to select an element if it is the '''target''' of the current page URL. This is really useful and allows for some cool effects, because it effectively allows you to set styles to be applied when links are clicked. For example:

<pre>&lt;a href="#target"&gt;Click me&lt;/a&gt;

<div id="target">Woot!</div></pre>

Here we have a simple link followed by a <code>&lt;div&gt;</code> — the link references the <code>&lt;div&gt;</code> via it's ID. The current URL only targets the <code>&lt;div&gt;</code> upon the link being clicked. To style the <code>&lt;div&gt;</code> only when the link is clicked, you could use the following:

<pre>div:target {
  ...
}</pre>

To see a much more involved example of <code>:target</code> usage, read [http://dev.opera.com/articles/view/css3-target-based-interfaces/ CSS3 target-based interfaces] by Corey Mwamba.

=== UI element state pseudo-classes ===

These pseudo-classes are all concerned with styling advanced states of UI elements. You'll most commonly use them to style HTML form elements, particularly when some of the new features of HTML5 forms are being used, such as built in validation (see [HTML5 form additions] for more details).

Let's say we are styling a basic form input with a <code>valid</code> attribute for validation:

<pre>&lt;input type="text" required&gt;</pre>

We could style it only when the information entered into it is valid or invalid using

<pre>input:valid {}</pre>

and 

<pre>input:invalid {}</pre>

We could style it depending on whether it is enabled (default) or disabled (using the <code>disabled</code> attribute), using

<pre>input:enabled {}</pre>

and 

<pre>input:disabled {}</pre>

Finally, we could style a checkbox only when checked like so:

input[type="checkbox"]:checked {}


=== Structural pseudo-classes ===

Structural pseudo-classes are advanced selectors allowing you to target specific elements based on their position in the document hierarchy. These were introduced in CSS3, and build on selectors we've already looked at, such as the adjacent sibling selector.

<code>:root</code> selects the root element of the document, which is usually the <code>&lt;html&gt;</code> element. For example:

<pre>html:root{ ... }</pre>

<p><code>:nth-child(n)</code> allows you to select a repeating pattern of elements inside an continuous set of like elements, for example several list items, or several paragraphs or articles next to one another. Let's look at an example:

<pre>&lt;ul&gt;
  &lt;li&gt;First&lt;/li&gt;
  &lt;li&gt;Second&lt;/li&gt;
  &lt;li&gt;Third&lt;/li&gt;
  &lt;li&gt;Fourth&lt;/li&gt;  
  &lt;li&gt;Fifth&lt;/li&gt;
  &lt;li&gt;Sixth&lt;/li&gt;
  &lt;li&gt;Seventh&lt;/li&gt;
  &lt;li&gt;Eighth&lt;/li&gt;
  &lt;li&gt;Ninth&lt;/li&gt;
  &lt;li&gt;Tenth&lt;/li&gt;
&lt;/ul&gt;</pre>

<code>n</code> is set to the pattern we want to select. In this case, to select list items we do this:

<pre>li:nth-child(n)</pre>

To select just the odd or even list items, we'd use these:

<pre>li:nth-child(odd)
li:nth-child(even)</pre>

Or we could use

<pre>li:nth-child(2n+1)
li:nth-child(2n+0)</pre>

To do the same thing.

Let's look at some other formula examples:

* <code>li:nth-child(5)</code>: select the 5th adjacent list item
* <code>li:nth-child(4n+1)</code>: select every 4th list item, and then add 1 to each result. So numbers 5 and 9.
* <code>li:nth-child(3n-2)</code>: select every 3rd list item, and subtract 2 from each result. So numbers 1, 4 and 7.

Next let's move on to <code>nth-last-child(n)</code>. This does the same thing as <code>nth-child(n)</code>, but it counts from the last element in the sequence, not the first.

<code>nth-of-type(n)</code> and <code>nth-last-of-type(n)</code> do pretty much exactly the same thing as <code>nth-child(n)</code> and <code>nth-last-child(n)</code>, but there is one important difference: the former two ignore any rogue elements interspersed with the repeated sequence of like elements because they select by type of element, not child number. The latter selects by child number.

Let's have a look at another example:

<pre>&lt;div&gt;
  1. &lt;article class="abstract"&gt; ... &lt;/article&gt;
  2. &lt;article class="abstract"&gt; ... &lt;/article&gt;
  3. &lt;article class="abstract"&gt; ... &lt;/article&gt;
  4. &lt;article class="abstract"&gt; ... &lt;/article&gt;
  5. &lt;article class="abstract"&gt; ... &lt;/article&gt;
  6. &lt;blockquote&gt;&lt;p&gt; ... &lt;/p&gt;&lt;/blockquote&gt;
  7. &lt;article class="abstract"&gt; ... &lt;/article&gt;
  8. &lt;article class="abstract"&gt; ... &lt;/article&gt;
  9. &lt;article class="abstract"&gt; ... &lt;/article&gt;
&lt;/div&gt;</pre>

In this example we've got a <code>&lt;element&gt;</code> with eight child <code>&lt;article&gt;</code> elements, and a single <code>&lt;blockquote&gt;</code> element sat in the middle of them: this is child number six. There are a total of nine child elements.

If you used <code>article:nth-child(2n+0)</code> as your selector, to select all the even-numbered children of the <code>&lt;div&gt;</code>, you'd select only the <code>&lt;article&gt;</code>s in positions 2, 4 and 8: the <code>&lt;blockquote&gt;</code> (position number six) wouldn't be selected because it is not an <code>&lt;article&gt;</code>.

If you used <code>article:nth-of-type(2n+0)</code> as your selector, you would select the <code>&lt;article&gt;</code>s in positions 2, 4, 7 and 9: this is because this selects by the type of element, not the child position, therefore in this case the <code>&lt;blockquote&gt;</code> is completely ignored and the even numbered <code>&lt;article&gt;</code>s are selected. Yes, two of them are odd numbered according to my original numbering scheme because in reality the <code>&lt;blockquote&gt;</code> exists and offsets their position, but <code>article:nth-of-type(2n+0)</code> ignores the <code>&lt;blockquote&gt;</code>, effectively counting positions 7 and 9 as 6 and 8. 

Next, we’ll have a look at <code>:first-child</code> and <code>:last-child</code> — these pseudo-classes select only the first or last instance of an element that is the first or last child element of its parent. So, considering the above example again, we could use the following to select - respectively - the first and last <code>&lt;article&gt;</code> element:

 
<pre>article:first-child { ... }

article:last-child { ... }</pre>

<code>blockquote:first-child</code> would select nothing, because the first child is not a <code>&lt;blockquote&gt;</code>.

<code>first-of-type</code> and <code>last-of-type</code> again work in a very similar way, but they select based on the type of element, not the position of child it is. So <code>article:first-of-type</code> would select exactly the same <code>&lt;article&gt;</code> element as <code>article:first-child</code>, but <code>blockquote:first-of-type</code> would select the single <code>&lt;blockquote&gt;</code> in the example, because it is the first of its type, even thought it is the 6th child.

There are a few others to quickly consider:

* <code>only-child</code>: Selects an element only if it is the only child of it's parent, eg <code>article:only-child</code> wouldn't select anything in our example above, because there is more than one <code>&lt;article&gt;</code> child.
* <code>only-of-type</code>: Selects an element only if it is the only sibling of it's type inside the parent element. eg <code>blockquote:only-of-type</code> would select the <code>&lt;blockquote&gt;</code> in the above example because it is the only one of its type present.
* <code>empty</code>: selects an element only if it has no children whatsoever (including text nodes). For example <code>div:empty</code> would select <code>&lt;div&gt;&lt;/div&gt;</code>, but not <code>&lt;div&gt;1&lt;/div&gt;</code> or <code>&lt;div&gt;&lt;p&gt;Hi!&lt;/p&gt;&lt;/div&gt;</code>
 
== Pseudo-elements ==
 
Pseudo elements differ from pseudo-classes in that they don't select states of elements; they select parts of an element.

=== :first-letter ===

First of all, you can select the first letter inside a given element using the following rule:
 
<pre>p:first-letter {
  font-weight: bold;
  font-size: 300%
  background-color: red;
}</pre>
 
The first letter of every paragraph will now be bolded, 300% bigger than the rest of the paragraph, and have a red background. This is a good start towards creating a decent drop cap effect.

=== :first-line ===
 
To make the first line of every paragraph bold, you could use the following rule:
 
<pre>p:first-line {
  font-weight: bold;
}</pre>

=== Generated content using :before and :after ===
 
You can use the <code>:before</code> and <code>:after</code> pseudo-elements to specify that content should be inserted before and after the element you are selecting. You then specify what content you want to insert or generate. As a simple example, you can use the following rule to insert a decorative image after every link on the page:

<pre>a:after {
  content: " " url(flower.gif);
}</pre>
 
You can also use the <code>attr()</code> function to insert the values of attributes of the elements after the element. For example, you could insert the target of every link in your document in brackets after each one using the following:
 
<pre><code>a:after {
  content: "" "(" attr(href) ")";
}</code>
</pre>
 
This is a great technique to use in a print stylesheet, where you want to just show the URLs in the document rather than have them hidden inside links (useless on a printed page).

You can also insert incremented numerical values after repeating elements (such as bullets or paragraphs) using the <code>counter()</code> function — this is explained in much more detail in [[http://dev.opera.com/articles/view/automatic-numbering-with-css-counters/ Automatic numbering with CSS counters]] by David Storey.
 
These selectors are not supported in IE 7 or below. Also note that you shouldn't insert important information with CSS, or that content will be unavailable to assistive technologies or if a user chooses not to use your stylesheet. The golden rule is that CSS is for styling; HTML is for important content.

=== CSS3 pseudo-element double colon syntax ===

Please note that the new CSS3 way of writing pseudo-elements is to use a double colon, eg <code>a::after { ... }</code>, to set them apart from pseudo-classes. You may see this sometimes in CSS. CSS3 however also still allows for single colon pseudo-elements, for the sake of backwards compatibility, and we would advise that you stick with this syntax for the time being.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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