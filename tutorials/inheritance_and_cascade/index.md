{{Flags}}
{{Summary_Section|This guide explain inheritance and the cascade, two fundamental concepts in CSS.}}
{{Guide
|Content=== Introduction ==
 
Inheritance and the cascade are two fundamental concepts in CSS, which everyone using the technology needs to understand. The two concepts are closely related, yet different:

* Inheritance is associated with how the elements in the HTML markup inherit properties from their parent (containing) elements and pass them on to their children
* The cascade has to do with the CSS declarations being applied to a document, and how conflicting rules do or don’t override each other.
 
Here we will look closely at both concepts. [http://dev.opera.com/articles/view/28-inheritance-and-cascade/inheritance_cascade_code.zip Download the source code for the examples] in this article; the zip contains the finished CSS and HTML, as well as the initial HTML template for you to work with as you go through the examples.

== Inheritance ==
 
Inheritance is the mechanism by which certain properties are passed on from a parent element down to its children, in the same fashion as genetics: if the parents have blue eyes, their children will probably have blue eyes.
 
Not all CSS properties are inherited, because it doesn’t make sense for some of them to be. For instance, margins and width are not inherited, since it’s unlikely that a child element should need the same margins as its parent. Imagine if you set the content block of a site to be 70% of the browser window width, and then had all of it's children adopting a width of 70% of their parents? Doing page layouts with CSS would be a nightmare.

In most cases common sense will tell you which properties are inherited and which aren’t: if you are not sure you can look up all of the properties present in CSS2 in the [http://www.w3.org/TR/CSS21/propidx.html CSS 2.1 specification property summary table]. For CSS3 properties, you'll have to consult the individual CSS3 module specifications, available in the [http://www.w3.org/Style/CSS/current-work CSS current work page].
 
=== Why inheritance is useful ===
 
So why does CSS have an inheritance mechanism? The easiest way to answer that is probably to consider what it’d be like if there was no such thing as inheritance. You would have to specify things like font family, font size and text color individually — for every single element type.
 
Using inheritance, you can for example specify the font properties for the <code>html</code> or <code>body</code> elements and they will be inherited by all other elements. You can specify background and text colors for a specific container element and the text color will automatically be inherited by any child elements in that container. The background color isn’t inherited, but the initial value for <code>background-color</code> is <code>transparent</code>, which means the parent’s background will shine through. The effect is similar to what you’d get if the background color were inherited.

Note: consider what would happen if background ''images'' were inherited? Every child would have the same background image as its parent and the result would look like a jigsaw puzzle put together by someone with a serious drug problem, since the background would be redrawn inside each subsequent child element.
 
=== How inheritance works ===
 
Every element in an HTML document will inherit all inheritable properties from its parent ''except'' the root element (<code>&lt;html&gt;</code>), which doesn’t have a parent.
 
Whether or not the inherited properties will have any effect depends on other things, as you shall see later on when we talk about the cascade. Just as a blue-eyed mother can have a brown-eyed child if the father has brown eyes,

inherited properties in CSS can be overridden.
 
=== An example of inheritance ===
 
# Copy the following HTML document into a new file in your favourite text editor and save it as inherit.html.

<pre>&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
  &lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;title&gt;Inheritance&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
   &lt;h1&gt;Heading&lt;/h1&gt;
   &lt;p&gt;A paragraph of text.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;</pre>

If you open the document in your web browser you will see a rather boring document displayed according to your browser’s default styling.

# Create a new empty file in your text editor, copy the CSS rule below into it, and save the file as style.css in the same location as the HTML file.

<pre>html {
  font: 75% Verdana, sans-serif;
}</pre>

# Link the style sheet to your HTML document by inserting the following line before the <code>&lt;/head&gt;</code> tag:

<pre>&lt;link rel="stylesheet" type="text/css" href="style.css"&gt;</pre>

# Save the modified HTML file and reload the document in your browser.

The font will change from the browser’s default (often Times or Times New Roman) to Verdana.

If you don’t have Verdana installed on your computer, the text will be displayed in the default sans serif font specified in your browser settings. The text will also become smaller; only three quarters of what it was in the unstyled version. The CSS rule we specified applies only to the <code>&lt;html&gt;</code> element. We didn’t specify any rules for headings or paragraphs, yet all the text now displays in Verdana at 75% of the default size. Why? Because of inheritance. The <code>font</code> property is a shorthand property that sets a whole number of font-related properties.

We’ve only specified two of them — the font size and the font family—but that rule is equivalent to the following:

<pre>html {
  font-style: normal;
  font-variant: normal;
  font-weight: normal;
  font-size: 75%;
  line-height: normal;
  font-family: Verdana,sans-serif;
}</pre>

All of those properties are inherited, so the <code>&lt;body&gt;</code> element will inherit them from the <code>&lt;html&gt;</code> element and then pass them on to its children — the heading and the paragraph. But wait a second! There’s something fishy going on with the inheritance of font size, isn’t there?

The <code>&lt;html&gt;</code> element’s font size is set to 75%, but 75% of ''what''? Surely the font size of the <code>&lt;body&gt;</code> should be 75% of its parent’s font size, and the font sizes of the heading and the paragraph be 75% of that of the <code>&lt;body&gt;</code> element? The value inherited is not the specified value — the value we write in our style sheet — but something called the computed value.

The computed value is, in the case of font size, an absolute value measured in pixels. For the <code>&lt;html&gt;</code> element, which doesn’t have a parent element from which to inherit, a percentage value for font size relates to the default font size set in the browser. Most contemporary browsers have a default font size setting of 16px. 75% of 16 is 12, so the computed value for the font size of the <code>&lt;html&gt;</code> element will be around 12px.

And ''that'' is the value that is inherited by <code>&lt;body&gt;</code> and passed on to the heading and the paragraph. (The font size of the heading is larger, because the browser applies some built-in styling of its own. See the discussion about the cascade, below.)

# Add two more declarations to the rule in your CSS style sheet:

<pre>html {
  font: 75% Verdana,sans-serif;
  '''background-color: blue;
  color: white;'''
}</pre>

# Save the CSS file and reload the document in your browser. Now the background of the whole document is bright blue, and all the text is white. The white text color is inherited by the <code>&lt;body&gt;</code> element and passed on to all children of <code>body</code> — in this case the heading and the paragraph. The heading and paragraph don’t however inherit the background but instead will default to <code>transparent</code>, so the net visual result will be white text on a blue background.

# Add another new rule to the style sheet:

<pre>h1 {
  font-size: 300%;
}</pre>

Save and reload the document: this rule sets the font size for the heading. The percentage is applied to the inherited font size — 12px, as we discussed above — so the heading size will be 300% of 12px, or 36px.

=== Forcing inheritance ===
 
You can force inheritance — even for properties that aren’t inherited by default — by using the <code>inherit</code> keyword. This should be used with care, however, since Microsoft Internet Explorer versions up to and including version 7 don’t support this keyword.
 
The following rule will make all paragraphs inherit all background properties from their parents:
 
<pre>p {
  background: inherit;
}</pre>
  
Forcing inheritance isn’t something you need to do every day. It can be useful for “undoing” a declaration in a conflicting rule, or to avoid hardcoding certain values. As an example, consider a typical navigation menu:
 
<pre>&lt;ul id="nav"&gt;
  &lt;li&gt;&lt;a href="/"&gt;Home&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="/news/"&gt;News&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="/products/"&gt;Products&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="/services/"&gt;Services&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="/about/"&gt;About Us&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;</pre>
 
To display this list of links as a horizontal menu, you could use the following CSS:
 
<pre>#nav {
  background: blue;
  color: white;
  margin: 0;
  padding: 0;
}

#nav li {
  display: inline;
  margin: 0;
  padding: 0 0.5em;
  border-right: 1px solid;
}

#nav li a {
  color: inherit;
  text-decoration: none;
}</pre>
 
Here the background color of the whole list is set to blue in the rule for <code>#nav</code>. This also sets the foreground color to white, and this is inherited by each list item and each link. The rule for the list items sets a right border, but doesn’t specify the border color, which means it will use the inherited foreground color, white. For the links we’ve used <code>color:inherit;</code> to force inheritance and override the browser's default link color.

Of course I could just as well have specified the border color as white and the link text color as white, but the beauty of letting inheritance do the job is that you now have only one place to change the colors if you decide to update the color scheme at a later date.

== The cascade ==
 
CSS an acronym of Cascading Style Sheets, so it shouldn’t come as a surprise that the cascade is an important concept. It’s the mechanism that controls the end result when multiple, conflicting CSS declarations apply to the same element. There are three main concepts that control the order in which CSS declarations are applied:
 
# Importance
# Specificity
# Source order
 
We'll look at these concepts below, one by one.
 
Importance is most … er … important. If two declarations have the same importance, the specificity of the rules decide which one will apply. If the rules have the same specificity, then source order controls the outcome.
 
=== Importance ===
 
The importance of a CSS declaration depends on ''where'' it is specified. The conflicting declarations will be applied in the following order, with later ones overriding earlier ones:
 
# User agent style sheets
# Normal declarations in user style sheets
# Normal declarations in author style sheets
# Important declarations in author style sheets
# Important declarations in user style sheets

==== User agent style sheets ====
 
A user agent style sheet is the built-in style sheet of the browser. Every browser has its default rules for how to display various HTML elements if no style is specified by the user or designer of the page. For instance, unvisited links are usually blue and underlined.
 
A user style sheet is a style sheet that the ''user'' has specified. Not all browsers support user style sheets, but they can be very useful, especially for users with certain types of disabilities. For instance, a dyslexic person can have a user style sheet that specifies certain fonts and colors that help reading.
 
Note: Opera allows you to specify user stylesheets by going to Tools (or the Opera menu on the Mac) &gt; Preferences… &gt; Advanced tab &gt; Content, clicking on the Style Options… button, then pointing to your user style sheet in the My style sheet text field inside the Display tab of this dialog box. You can also specify if you want the user style sheet to override the author (web designer’s) stylesheet in the Presentation tab, and even add a button into the user interface that allows you to switch between the user and author style sheet.

To do this, OK out of the Preferences… menu completely, then right- or Ctrl-click somewhere on the Opera browser interface, select Customize… &gt; Buttons tab &gt; Browser view, and drag the Author Mode button somewhere on to one of your toolbars.
 
An author style sheet is what we normally refer to when we say “style sheet”. It’s the style sheet that the author of the document (or, more likely, the site’s designer) has written and linked to (or included).

==== Normal and important declarations ====

Normal declarations are just that: normal declarations.

The opposite is important declarations, which are declarations followed by an <code>!important</code> directive. A dyslexic user might, for instance, want all text to be displayed in Comic Sans MS if he finds that font easier to read. He could then have a user style sheet containing the following rule:
 
<pre>* {
  font-family: "Comic Sans MS" !important;
}</pre>

Important declarations in a user style sheet will trump everything else, which is logical. In this case, no matter what the designer specified, and no matter what the browser’s default font family is set to, everything will be displayed in Comic Sans MS. The default browser rendering will only apply if those declarations aren’t overridden by any rules in a user style sheet or an author style sheet, since the user agent style sheet has the lowest precedence.
 
To be honest, most designers don’t have to think too much about importance, since there’s nothing we can do about it. There is no way we could know if a user has a user style sheet defined that will override our CSS. If they do, they probably have a very good reason for doing so, anyway. Still, it’s good to know what importance is and how it may affect the presentation of our documents.
 
=== Specificity ===
 
Specificity is something every CSS author needs to understand and to think about. It can be thought of as a measure of how specific a rule’s selector is. A selector with low specificity may match many elements (like <code>*</code>, which matches every element in the document), while a selector with high specificity might only match a single element on a page (like <code>#nav</code>, which only matches the element with an <code>id</code> of <code>nav</code>).

The specificity of a selector can easily be calculated, as we shall see below. If two or more declarations conflict for a given element, and all the declarations have the same importance, then the one in the rule with the most specific selector will “win”.
 
Specificity has four components; let’s call them a, b, c and d. Component “a” is the most distinguishing, “d” the least.
 
* Component “a” is quite simple: it’s 1 for a declaration in a <code>style</code> attribute, otherwise it’s 0.
* Component “b” is the number of <code>id</code> selectors in the selector (those that begin with a <code>#</code>). 
* Component “c” is the number of attribute selectors—including class selectors — and pseudo-classes.
* Component “d” is the number of element types and pseudo-elements in the selector.
 
After a bit of counting, we can thus string those four components together to get the specificity for any rule. CSS declarations in a <code>style</code> attribute don’t have a selector, so their specificity is always 1,0,0,0.
 
Let’s look at a few examples — after this it should be quite clear how this works.

                                    
{| border="1"
|-
!Selector
!a
!b
!c
!d
!Specificity
|-
|<code>h1</code>
| 
| 
| 
|1
|0,0,0,1
|-
|<code>.foo</code>
| 
| 
|1
| 
|0,0,1,0
|-
|<code>#bar</code>
| 
|1
| 
| 
|0,1,0,0
|-
|<code>html&gt;head+body ul#nav *.home a:link</code> 
| 
|1
|2
|5
|0,1,2,5
|}

Let’s look at the last example in some more detail. a = 0 since it’s a selector, not a declaration in a <code>style</code> attribute. There is one ID selector (<code>#nav</code>), so b = 1. There is one attribute selector (<code>.home</code>) and one pseudo-class (<code>:link </code> ), so c = 2. There are five element types (<code>&lt;html&gt;</code>, <code>&lt;head&gt;</code>, <code>&lt;body&gt;</code>, <code>&lt;ul&gt;</code> and <code>&lt;a&gt;</code>), so d = 5.

The final specificity is thus 0,1,2,5.

Note: Combinators (like <code>&gt;</code>, <code>+</code> and white space) do not affect a selector’s specificity. The universal selector (<code>*</code>) has no input on specificity, either.
 
Note #2: There is a huge difference in specificity between an <code>id</code> selector and an attribute selector that happens to refer to an <code>id</code> attribute. Although they match the same element, they have very different specificities. The specificity of <code>#nav</code> is 0,1,0,0 while the specificity of <code>[id="nav"]</code> is only 0,0,1,0.
 
Let’s look at how this works in practice.
 
First of all, start by adding another paragraph to your HTML document.

<pre><code>&lt;body&gt;
  &lt;h1&gt;Heading&lt;/h1&gt;
  &lt;p&gt;A paragraph of text.&lt;/p&gt;
  '''&lt;p&gt;A second paragraph of text.&lt;/p&gt;'''
&lt;/body&gt;</code> </pre>

Next, add a rule to your stylesheet to make the paragraph text have a different color:

<pre><code>p {
  color: cyan;
}</code> </pre>

Now save both files and reload the document in your browser; there should now be two paragraphs with cyan text.

Set an <code>id</code> on the first paragraph so you can target it easily with a CSS selector.

<pre>&lt;body&gt;
  &lt;h1&gt;Heading&lt;/h1&gt;
  &lt;p '''id="special"'''&gt;A paragraph of text.&lt;/p&gt;
  &lt;p&gt;A second paragraph of text.&lt;/p&gt;
&lt;/body&gt;</pre>

Carry on by adding a rule for the special paragraph in your style sheet:

<pre>#special {
  background-color: red;
  color: yellow;
}</pre>

Finally, save both files and reload the document in your browser to see the now rather colorful result.
 
Let’s look at the declarations that apply to the two paragraphs.
 
The first rule you added sets a text color of cyan for ''all'' paragraphs. The second rule sets a red background color and a yellow text color for the single element that has the <code>id</code> of <code>special</code>. Your first paragraph matches both of those rules; it is a paragraph and it has an <code>id</code> of <code>special</code>.
 
The red background isn’t a problem, because it’s only specified for <code>#special</code>. Both rules contain a declaration of the <code>color</code> property, though, which means there is a conflict. Both rules have the same importance — they are normal declarations in the author style sheet — so you have to look at the specificity of the two selectors.

The selector of the first rule is <code>&lt;p&gt;</code>, which has a specificity of 0,0,0,1 according to the rules above since it contains a single element type. The selector of the second rule is <code>#special</code>, which has a specificity of 0,1,0,0 since it consists of an <code>id</code> selector. 0,1,0,0 is much more specific than 0,0,0,1 so the <code>color: yellow;</code> declaration wins and you get yellow text on a red background.

=== Source order ===
 
If two declarations affect the same element, have the same importance and the same specificity, the final distinguishing mark is the source order. The declaration that appears later in the style sheets will “win” over those that come before it.
 
If you have a single external style sheet, then the declarations at the end of the file will override those that occur earlier in the file if there’s a conflict. The conflicting declarations could also occur in different style sheets.

In that case, the order in which the style sheets are linked, included or imported controls what declaration will be applied, so if you have two stylesheets linked in a document <code>&lt;head&gt;</code>, the one linked to further down will override the one linked to higher up. Let’s look at a practical example of how this works.
 
# Add a new rule to your style sheet at the very end of the file, like so:

<pre>p {
  background-color: yellow;
  color: black;
}</pre>

# Save and reload the web page. you will now have ''two'' rules that match all paragraphs. They have the same importance and the same specificity (since the selector is the same), therefore the final mechanism for choosing which one wins will be the source order. The last rule specifies <code>color:black</code> and that will override <code>color:cyan</code> from the earlier rule.
 
Note how the first paragraph isn’t affected at all by this new rule.

Although the new rule appears last, its selector has lower specificity than the one for <code>#special</code>. This shows clearly how specificity trumps source order.
 
== Summary ==
 
Inheritance and the cascade are fundamental concepts that every web designer should understand.
 
Inheritance lets us declare properties on high-level elements and allows those properties to trickle down and style descendant elements. Only some properties are inherited by default, but inheritance can be forced with the <code>inherit</code> keyword.
 
The cascade sorts out all conflicts when multiple declarations would affect a given element. Important declarations will override less important ones. Among declarations with equal importance, the rule’s specificity controls which one will apply.

All else being equal, the source order makes the final distinction.
 

}}
{{See_Also_Section
|Manual_sections==== Exercise Questions ===
 
* Is the <code>border</code>  property inherited? Think about it first—would it make sense?—then look up the correct answer in the [http://www.w3.org/TR/CSS21/ CSS specification].
* If we add <code>!important</code> to the <code>color:black</code> declaration in the last rule in our [http://dev.opera.com/articles/view/28-inheritance-and-cascade/inheritance_cascade_code.zip example style sheet], will this have any effect on the text color in the first, “special” paragraph?
* Which selector is more specific, “<code>#special</code>” or “<code>html&gt;head+body&gt;h1+p</code>”?
* What should a user style sheet look like to make our test document display in black Comic Sans MS on a white background, regardless of the author style sheet?
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}