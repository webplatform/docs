{{Page_Title|Getting started with CSS}}
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
{{Summary_Section|This guide covers the basic fundamentals of CSS, including CSS anatomy, selectors, and comments, and shows how to apply CSS rules to HTML content.}}
{{Tutorial
|Next_page=
|Prev_page=
|Content=== Introduction ==

This article covers the basics of CSS to help you get started with this powerful styling language. You will learn how to apply CSS to HTML documents, 
either as inline styles using <code>style</code> attributes, embedded styles in a <code>&lt;style&gt;</code> element in the document 
<code>&lt;head&gt;</code>, or as external files in their own documents.

You will also learn that the latter method — linking an external style sheet using a <code>&lt;link&gt;</code> element — makes the most 
sense in terms of maintenance and caching.

Additionally, an overview of the basic syntax of CSS is provided, including details about adding comments, selector types, and grouping selectors.
 
== Review: What is CSS? ==
 
While HTML structures the document and tells browsers the function of page elements, CSS provides rules that instruct the browser how to display 
the elements — styling, spacing, coloring, etc. If HTML is the foundation and bricks that make up the structure of a house, CSS is the plaster and 
paint that decorate it.
 
CSS styles are applied using a system of rules. CSS rules:

* Identify which HTML elements should have styling applied
* Specify the "properties" (color, size, font, and other attributes) of the styled HTML elements 
* Contain the values that control the appearance of each property

For example, a CSS rule might state:

''I want to find every <code>&lt;h2&gt;</code> element on a page, and change the color of text surrounded by these tags to green.''

or

''I want to find every <code>&lt;p&gt;</code> element with a class attribute of <code>author-name</code>, set the background color to red, resize the text to twice the size of normal paragraph text, and add 10 pixels of spacing around it.''

CSS is not a markup language like HTML, nor is it a procedural programming language like JavaScript. 
It is a declarative language that uses its own logic to identify and locate the page elements to which its style rules should be applied. 
Older technologies that defined interfaces before modern web development came along always mixed presentation and structure. 
As we've discussed in other tutorials, this is not a wise choice in an environment that changes as often as the web, which is why CSS was invented.
 
== Defining style rules ==
 
Style rules can operate on different sets of items, selected in different ways. For example, they can be directly applied to HTML elements (body, 
article, nav, list, p, em, strong, etc.), or they can be applied to any elements with custom classes or IDs.  This is the basic form:

<syntaxhighlight lang="css">selector {
  property1: value;
  property2: value;
  property3: value;
}</syntaxhighlight>
 
The pertinent parts are as follows:

* The ''selector'' identifies which HTML elements are affected by the rule, using actual element names such as <code>&lt;body&gt;</code>, or other identifiers such as <code>class</code> attribute values. When applied to the element names, ''selector'' is simply replaced by the name of that block.  For classes, the syntax is <code>.classname</code>; for IDs, <code>#idname</code>.  A more complete description comes later.
* The braces contain the ''property:value'' pairs, which are separated from each other by semi-colons; the properties are separated from their respective values by colons.
* The ''properties'' define what you want to do to the selected element(s). These can affect attributes such as text color, background color, the position of the element on the page, font type, border color and thickness, and many other appearance and layout characteristics.
* The ''values'' are the settings that specify details of each property applied to elements, and the values are dependent on the property. For example, properties that affect color can use hexadecimal colors like <code>#336699</code>, RGB values like <code>rgb(12,134,22)</code> or color names like <code>red</code>, <code>green</code>, or <code>blue</code>. Properties that affect position, margins, width, height, and others can be measured in pixels, ems, percentages, centimeters, or other units.
 
Review this example:
 
<syntaxhighlight lang="css">p {
  margin: 5px;
  font-family: arial;
  color: blue;
}</syntaxhighlight>
 
The HTML element this rule affects is <code>&lt;p&gt;</code> — every <code>&lt;p&gt;</code> in the HTML document or documents that this CSS rule is 
applied to will display with these styles, unless they have more specific rules also applied to them (more about that later). 
The properties affected by this rule are the margins around the paragraphs, the font of the text inside the paragraph tags, and the color of the
text. The margins are set to 5 pixels, the font is set to Arial, and the color of the text is set to blue.

A group of CSS rules can be added to a CSS document to form a style sheet. This is the most basic syntax when writing CSS rules. 
Some rules are more complex, but not much — one of the best things about CSS is its simplicity.
 
=== Whitespace in CSS ===

Whitespace in CSS works in exactly the same way as it does in HTML. Excess whitespace is completely ignored by the browser that renders the CSS, 
so in most cases you can add as much whitespace as you like to make the code easier to read. So this rule:

<syntaxhighlight lang="css">p {
  margin: 5px;
  font-family: arial;
  color: blue;
}</syntaxhighlight>

is functionally identical to this rule: 

<syntaxhighlight lang="css">p {margin: 5px;font-family: arial;color: blue;}</syntaxhighlight>

There are a few exceptions where whitespace matters, for example, inside CSS function syntax. The property value 
<code>url(background-image.png)</code> would not work properly if you put a space between url and the opening parenthesis, 
as in <code>url (background-image.png)</code>.  But in general, as long as you include the necessary braces, colons, and semi-colons 
to separate the different parts, the browser understands the values you apply to properties. 

=== CSS comments ===
 
One thing to know early on is how to add comments in CSS. As in any language, comments can help clarify the intent of the code.
You add comments by enclosing them in <code>/*</code> and <code>*/</code> delimiters. Comments can span several lines. 
Browsers will ignore commented lines of text:
 
<syntaxhighlight lang="css">/* This is basic CSS rule syntax */
selector{
  property1: value;
  property2: value;
  property3: value;
}</syntaxhighlight>
 
You can add comments either between rules or inside the property block. For example, in the following CSS the second and third properties 
are enclosed inside comment delimiters, so they will be ignored by the browser. This is useful when you are testing the effect certain CSS 
rules have on your web page; just comment them out, save your CSS file, and reload the HTML page in a browser.

<syntaxhighlight lang="css">selector{
  property1: value;
  /* 
  property2: value;
  property3: value;
  */
}</syntaxhighlight>

=== Grouping selectors ===
 
You can also group selectors. If you want to apply the same style to <code>h1</code> and <code>p</code>, you can use the following CSS:
 
<syntaxhighlight lang="css">h1 {
  color: red;
}

p {
  color: red;
}</syntaxhighlight>
 
This, however, is not ideal coding practice, as you are repeating the same information. To remedy this, you can shorten the CSS by 
grouping the selectors together with a comma — the rules within the braces are then applied to both selectors:

<syntaxhighlight lang="css">h1, p {
  color: red;
}</syntaxhighlight>

===Basic types of selectors===
 
There are several different types of selectors, each matching a different part of the markup. 
The three types of selectors that you will encounter most often are:

====Element selector====

<syntaxhighlight lang="css">p {}</syntaxhighlight>

An element selector matches all the elements of that name on the page (<code>&lt;p&gt;</code> elements, in the case above). 
By specifying an HTML element (tag) as a selector, you can affect all page content that is marked up with that tag.

====Class selector====

<syntaxhighlight lang="css">.example {}</syntaxhighlight>

A class selector matches all elements that have a <code>class</code> attribute with the value specified, so the above would match <code>&lt;p class="example"&gt;</code>, <code>&lt;li class="example"&gt;</code>, or <code>&lt;div class="example"&gt;</code>, or any other element with a <code>class</code> of <code>example</code>. Note that this type of class selector does not test for any specific element name.

====ID selector====

<syntaxhighlight lang="css">#example {}</syntaxhighlight>

An ID selector matches all elements that have an <code>id</code> attribute with the value specified, so the above would match 
<code>&lt;p id="example"&gt;</code>, <code>&lt;li id="example"&gt;</code>, <code>&lt;div id="example"&gt;</code>, or any other element with an 
<code>id</code> of <code>example</code>. Note that ID selectors do not test for any element name, but IDs must be unique within each HTML page.  

====Combining selectors====
 
You can join selectors together to define even more specific rules:

* <code>p.warning {}</code> &mdash; matches all paragraphs with a <code>class</code> of <code>warning</code>.
* <code>div#example {}</code> &mdash; matches the element with an <code>id</code> attribute of <code>example</code>, but only when it is a <code>div</code>. 
* <code>p.info, li.highlight {}</code> &mdash; matches paragraphs with a <code>class</code> of <code>info</code> and list items with a <code>class</code> of <code>highlight</code>.

Note that this does not mean you can use a shorthand for the definition of your elements in HTML.  For example, your HTML paragraph 
will still have to be in the form <code>&lt;p class="classname"&gt;</code>, but you can style it in your CSS with <code>p.classname {}</code>.

== CSS shorthand ==
 
Another thing you will come across regularly CSS shorthand. It is possible to combine several related CSS properties together into one property 
to save time and effort. In this section we will look at the available types of shorthand.
For more information, also see the [[guides/css_shorthand|CSS shorthand guide]] tutorial.
 
For example, this <code>border</code> property is shorthand:

<syntaxhighlight lang="css">border: 2px solid black;</syntaxhighlight>

It is equivalent to:

<syntaxhighlight lang="css">border-width: 2px;
border-style: solid;
border-color: black;</syntaxhighlight>
 
=== Comparing individual and shorthand values ===
 
Consider the following margin rule:
 
<syntaxhighlight lang="css">div.foo {
  margin-top: 1em;
  margin-right: 1.5em;
  margin-bottom: 2em;
  margin-left: 2.5em;
}</syntaxhighlight>
 
Such a rule could also be written as:
 
<syntaxhighlight lang="css">div.foo {
  margin: 1em 1.5em 2em 2.5em;
}</syntaxhighlight>
 
These types of property can take fewer than four values too, as follows:

* Same value applied to all four sides — <code>margin: 2px;</code>
* First value applied to the top and bottom, second to the left and right — <code>margin: 2px 5px;</code>.
* First and third values applied to the top and bottom respectively, second value applied to the left and right — <code>margin: 2px 5px 1px;</code>.
 
There are a number of properties that work like this, including <code>padding</code>, <code>margin</code> and <code>outline</code>. 

=== Making the choice to use a single property or a shorthand value ===
 
Shorthand <code>margin</code> and <code>padding</code> properties tend to get the greatest share of use, though there are situations in which 
shorthand properties are best avoided, or at least considered carefully, such as in the following situations:
 
* '''When a single margin needs to be set.''' In a situation where only one property needs to be set, the act of simultaneously setting multiple properties usually violates the KISS (Keep It Simple, Stupid) principle.
* '''The selector to which your properties apply is subject to many edge cases.''' When this happens — which it will, sooner or later — the inevitable heap of shorthand values can become hard to follow when it comes time to repair or alter your layout.
* '''The style sheet you're writing will be maintained by people with limited CSS skills.''' If you can get them to read this article you may not need to worry about this scenario, but it is best not to make any assumptions.
* '''You need to supplant a value, to account for an edge case.''' This requirement is often a signal of a poorly designed document or style sheet, but those are hardly rare.
 
== Applying CSS to HTML ==

The "C" in CSS stands for ''Cascading'', which refers to the method by which style rules flow downward, or cascade.
The order in which CSS rules are defined is important, and the methods you use to apply the rules defines their cascade sequence.

There are three ways to apply CSS to an HTML document: inline styles, embedded styles, and external style sheets. Unless you have a very 
good reason to use one of the first two, always go for the third option. The reason for this will become obvious soon, 
but here is an overview of the different options.
 
=== Inline styles ===
 
You can apply styles to a specific element using a <code>style</code> attribute, like this:
 
<syntaxhighlight lang="html5"><p style="background:blue; color:white; padding:5px;">Paragraph</p></syntaxhighlight>
 
Inside this attribute you list all the CSS properties and their values that you want to apply to the element. 
Each property/value pair is separated from the others by a semi-colon, and each property is separated from its value within each pair by a colon. 
If you open this example in a browser you will see that the paragraph with the <code>style</code> attribute is blue with white text and has a different size from the others, as shown in Figure 1.
 
[[Image:cssbasic.png|alt=Screenshot of the Opera browser showing an applied inline style sheet]]
 
''Figure 1: Opera shows the paragraph with the applied inline styles differently from the others.''
 
The benefit of inline styles is that the browser will be forced to use these settings regardless of other applicable styles. That is, any styles 
defined in other style sheets or even embedded in the <code>&lt;head&gt;</code> of the document will be overridden by these styles.
 
The big problem with inline styles is that they make maintenance a lot harder than it should be. Using CSS is all about separating the presentation 
of the document from the structure, but inline styles are doing just the opposite — scattering presentation rules throughout the document.
In addition to the maintenance issue, inline styles forfeit the advantage of the most powerful part of CSS: the cascade.

=== Embedded styles ===
 
Embedded styles are placed in the <code>&lt;head&gt;</code> of the document inside a <code>&lt;style&gt;</code> element,
as in this example:
 
<syntaxhighlight lang="css"><style type="text/css" media="screen">
  p {
    color: white;
    background: blue; 
    padding: 5px;
  }
</style></syntaxhighlight>
 
Here, the defined styles get applied to all the paragraphs in the document, as shown in Figure 2.
 
[[Image:cssbasid.png|Screenshot of the Opera browser showing how an embedded style sheet affects a lot of elements]]
 
''Figure 2: Opera shows all paragraphs with the styles defined in the embedded style sheet.''
 
The benefit with embedded styles is that you don't need to add a <code>style</code> attribute to each paragraph — you can style them all with a 
single definition. This also means that if you need to change the look and feel of all paragraphs, you can do it in one location. However, this is 
still limited to one document — what if you want to define the look of paragraphs for a whole site in one place? 
It is for this reason we use external style sheets.

=== External style sheets ===
 
External style sheets means putting all your CSS definitions in their own file, saving it with a file extension of <code>.css</code>, and then 
applying it to your HTML documents using a <code>&lt;link&gt;</code> element inside the document <code>&lt;head&gt;</code>. 
Let's have a closer look at that <code>&lt;link&gt;</code> element:
 
<syntaxhighlight lang="html5"><link rel="stylesheet" href="styles.css" type="text/css" media="screen"></syntaxhighlight>
 
The <code>href</code> attribute points to the CSS file, the <code>media</code> attribute defines which media should get these styles applied to it 
(<code>screen</code> in this case), and the <code>type</code> defines what the linked resource is (a file extension is not enough to determine that).
 
[[Image:cssbasie.png|Screenshot of the Opera browser showing how an external style sheet affects a lot of elements]]
 
''Figure 3: Opera shows the styles defined in the external style sheet when it is linked with a link element.''
 
This is the best of all worlds: you keep your look and feel definitions in one place, which means that you can make site-wide changes by 
changing one file, and the browser can load that once and then cache it for all other documents that reference it, meaning less to download.

=== Importing stylesheets ===
 
There is actually one more way to import external style sheets into HTML files: the <code>@import</code> property. 
This is inserted into an embedded style sheet, in the same way as the embedded CSS shown above. The syntax looks like this:
 
<syntaxhighlight lang="html5"><style type="text/css" media="screen">
  @import url("styles.css");

  /* ...other import statements or CSS styles could go here... */
   
</style></syntaxhighlight>
 
If you use
<code>@import</code>, it should always come first in an embedded style sheet. Also, you can specify that the imported style sheet be 
applied only to certain types of media by including the media type at the end of the import statement (this works in every browser except 
IE6 and below). The following does the same thing as the previous code example:
 
<syntaxhighlight lang="html5"><style type="text/css">
  @import url("styles.css") screen;

  /* ...other import statements or CSS styles could go here... */
   
</style></syntaxhighlight>
 
You may wonder, "Why on earth do I need another way to apply external style sheets to my HTML documents?" The answer is, you don't really. 
We are mainly including information on <code>@import</code> here for the sake of completeness. There are a few advantages and disadvantages 
of using <code>@import</code> over <code>&lt;link&gt;</code> elements, but they are ''very'' minor, so it is really up to you which way you go. 
In general, the <code>&lt;link&gt;</code> element is the recognised best way to do things these days.

A couple of notes about @import:
* IE6 doesn't support putting the media type at the end of the <code>@import</code> line, so this is not a good way to go if you want to insert multiple stylesheets for different media.
* You could argue that the code for multiple <code>@import</code> statements is smaller than the code for multiple <code>&lt;link&gt;</code> elements, but this is negligible.

==Conclusion==
You should now have a basic grasp of CSS rules, selectors, properties, and values. For more information on CSS,
see the other tutorials in this section.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=
|Chrome_supported=Yes
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=
|Android_supported=Yes
|Android_version=1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1.8
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=1
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections==== Exercise Questions ===
 
* What are the benefits and problems of inline styles and how do you apply them to an element?
* What is a style rule? Describe the different components and syntax.
* Say you have a bunch of style rules, what do you need to do to make them into an external style sheet?
* What does the following CSS selector match: <code>ul#nav{}</code>?
* What is the benefit of grouping selectors?
* How can you define a print style sheet?
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}