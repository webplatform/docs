{{Page_Title|CSS shorthand guide}}
{{Flags
|State=Almost Ready
|Editorial notes=Need to remove compatibility table; Need to crosslink to other relevant CSS content
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This short article covers the various bits of CSS shorthand you'll encounter in your day to day work.}}
{{Guide
|Content=== Border ==
 
<code>border</code> allows you to set border width, style and, color all in one single property. So for example:

<syntaxhighlight lang="css">border: 1px solid black;</syntaxhighlight>

is equivalent to the following three rules:

<syntaxhighlight lang="css">border-width: 1px;
border-style: solid;
border-color: black;</syntaxhighlight>

You can also break these down further into even more specific rules, for a single border of the element it is applied to, like so:

<syntaxhighlight lang="css">border-left: 1px solid black;
border-right: 1px solid black;
border-top: 1px solid black;
border-bottom: 1px solid black;</syntaxhighlight>

or even:

<syntaxhighlight lang="css">border-left-width: 2px;
border-left-style: solid;
border-left-color: black;</syntaxhighlight>

You will very rarely want to go this granular; you will probably use simply <code>border</code> or <code>border-left/right-top-bottom</code> in most cases. The more granular options will likely be used only if you want to override an earlier border declaration.

== Margin, padding, outline ==

 
Shorthand for <code>margin</code>, <code>padding</code>,  and <code>outline</code> all works in the same way. Consider the following <code>margin</code> rule:
 
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
 
These types of property can take less than four values too, as follows:

# Same value applied to all four sides — <code>margin: 2px;</code>
# First value applied to the top and bottom, second to the left and right — <code>margin: 2px 5px;</code>.
# First and third values applied to the top and bottom respectively, second value applied to the left and right — <code>margin: 2px 5px 1px;</code>.

== Font ==

You can specify the font size, weight, style, family, and line height using one line of shorthand. Consider the following CSS:

<syntaxhighlight lang="css">font-weight: bold;
font-style: italic;
font-variant: small-caps;
font-size: 1.5em;
line-height: 200%;
font-family: Georgia, "Times New Roman", serif;</syntaxhighlight>
 
You could specify all of this using the following line:

<syntaxhighlight lang="css">font: bold italic small-caps 1.5em/200% Georgia, "Times New Roman", serif;</syntaxhighlight>

Note that it doesn't really matter about the order of many of these, although you should make sure that <code>font-size</code>/<code>line-height</code> and <code>font-family</code> come in the positions shown, plus both <code>font-size</code> and <code>font-family</code> should be specified. If not, this shorthand may not work in some browsers.

Note also that if <code>font-weight</code>, <code>font-style</code> or <code>font-variant</code> are not specified, their values default to <code>normal</code>.

== Background ==

In CSS 2, you can specify background color, background image, image repeat and image position with one line of CSS. Take the following:

<syntaxhighlight lang="css">background-color: #000;
background-image: url(image.gif);
background-repeat: no-repeat;
background-position: top left;
background-attachment: fixed;</syntaxhighlight>
 
This can all be represented using the following shorthand:

<syntaxhighlight lang="css">background: #000 url(image.gif) no-repeat top left fixed;</syntaxhighlight>

Note that if any of the values are left out, the following defaults are assumed:

<syntaxhighlight lang="css">background-color: transparent;
background-image: none;
background-repeat: repeat;
background-position: top left;
background-attachment: scroll;</syntaxhighlight>

=== Enhancements in CSS3 ===

CSS3 introduces three new properties: [http://www.w3.org/TR/css3-background/#the-background-size <code>background-size</code>], [http://www.w3.org/TR/css3-background/#the-background-origin <code>background-origin</code>], and [http://www.w3.org/TR/css3-background/#the-background-clip <code>background-clip</code>]. You can include them in the <code>background</code> shorthand like so:

<syntaxhighlight lang="css">background: #000 url(image.gif); no-repeat top left / 50% 20% border-box content-box;</syntaxhighlight>

Notice the slash between <code>top left</code> and <code>50% 20%</code>; it separates the values for <code>background-position</code> and <code>background-size</code> since these two properties share some value units (lengths and percentage); without it we cannot distinguish which values are for which.

So if you want to include the <code>background-size</code> value in the shorthand syntax, you need to:

* Explicitly include <code>background-position</code> values even if these are the same as the defaults (see above).
* Write <code>background-position</code> values <em>before</em> <code>background-size</code> values.
* Put a slash in between these two pairs of values.

Similarly, <code>background-origin</code> and <code>background-clip</code> share the same keyword as their values. These two also needs to be written in order: <code>background-origin</code> coming in first, and <code>background-clip</code> second.

If you only specify one <code>box</code> value (<code>border-box</code>, <code>padding-box</code>, or <code>content-box</code>), then the value applies to <code>background-origin</code> and <code>background-clip</code>.

Note: CSS3 gradients are a special, advanced value of <code>background-image</code> — aside from the syntactical difference, gradient values appear in exactly the same place in the shorthand as other <code>background-image</code> values, and work in the same way. For more on CSS3 gradients, you can read [http://dev.opera.com/articles/view/css3-linear-gradients CSS3 linear gradients] and [http://dev.opera.com/articles/view/css3-radial-gradients/ CSS3 radial gradients] over at dev.opera.com.

== List ==

You can specify the list bullet type, position, and image on a single line. Take the following CSS:

<syntaxhighlight lang="css">list-style-type: circle;
list-style-position: inside;
list-style-image: url(bullet.gif);</syntaxhighlight>
 
This is the equivalent of:

<syntaxhighlight lang="css">list-style: circle inside url(bullet.gif);</syntaxhighlight>
 
Note that if any of the values are left out, the following defaults are assumed:

<syntaxhighlight lang="css">list-style-type: circle;
list-style-position: outside;
list-style-image: none;</syntaxhighlight>

== Color ==
 
When specifying hexadecimal color values, you can use shorthand if both hex values are the same for each color channel. For example, <code>#000</code> is equivalent to the longhand <code>#000000</code>. Let's look at a more complicated example too: <code>#6c9</code> is the same as <code>#66cc99</code>.
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