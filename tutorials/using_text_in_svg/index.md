{{Page_Title|Using text in SVG}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article details how to insert text into an SVG image.}}
{{Tutorial
|Content=When talking about text in SVG we have to differentiate two almost completely separate topics. The one is the inclusion and display of text in an image, and the other are SVG fonts. The later may be described in a later section of the tutorial, while we will focus completely on the first part: Bringing text into an SVG image.
 
=== Basics ===
 
We have seen in the [[introducing example]], that the <code>text</code> element can be used to put arbitrary text in SVG documents:
 
<pre>&lt;text x="10" y="10"&gt;Hello World!&lt;/text&gt;</pre>
 
The <code>x</code> and <code>y</code> attributes determine, where in the viewport the text will appear. The attribute <code>text-anchor</code>, which can have the values start, middle, end or inherit, allows to decide, in which direction the text flows from this point.
 
Like with the shape elements text can be colorized with the <code>fill</code> attribute and given a stroke with the <code>stroke</code> attribute. Both may also refer to gradients or patterns, which makes simple coloring text in SVG very powerful compared to CSS 2.1.
 
=== Setting font properties ===
 
An essential part of a text is the font in which it is displayed. SVG offers a set of attributes, many similar to their CSS counterparts, to enable font selection. Each of the following properties can be set as an attribute or via a CSS declaration: <code>font-family</code>, <code>font-style</code>, <code>font-weight</code>, <code>font-variant</code>, <code>font-stretch</code>, <code>font-size</code>, <code>font-size-adjust</code>, <code>kerning</code>, <code>letter-spacing</code>, <code>word-spacing</code> and <code>text-decoration</code>.
 
=== Other text-related elements ===
 
==== tspan ====
 
This element is used to mark up sub-portions of a larger text. It must be a child of a <code>text</code> element or another <code>tspan</code> element. A typical usecase is to paint one word of a sentence bold red.
 
<pre>&lt;text&gt;
  &lt;tspan font-weight="bold" fill="red"&gt;This is bold and red&lt;/tspan&gt;
&lt;/text&gt;</pre>
 
The tspan element has the following custom attributes:

'''x'''<br>
Set a new absolute x coordinate for the containing text. This overwrites the default current text position. The attribute may also contain a list of numbers, that are one by one applied to the single characters of the tspan element.
 
'''dx'''<br>
Start drawing the text with a horizontal offset dx from the default current position. Here, too, you may provide a list of values that are applied to consecutive characters, hence piling up the offset over time.
 
Likewise there are '''y''' and '''dy''' for vertical displacement.
 
'''rotate'''<br>
Rotate all charactes by this degree. A list of numbers makes each character rotate to its respective value, with remaining characters rotating according to the last value.
 
'''textLength'''<br>
This is a more obscure attribute giving the calculated length of the string. It is meant to allow the rendering engine to fine-tune the positions of the glyphs. when its own measured text length doesn't meet the one provided here.
 
===== tref =====
 
The <code>tref</code> element allows to reference already defined text, effectively copying it in its place. You can use the <code>xlink:href</code> attribute to point it to an element who's text content is to be taken over. You can then style it and modify it's appearance independent of the source.
 
<pre>&lt;text id="example"&gt;This is an example text.&lt;/text&gt;

&lt;text&gt;
    &lt;tref xlink:href="#example" /&gt;
&lt;/text&gt;</pre>
 
===== textPath =====
 
This element fetches via its <code>xlink:href</code> attribute an arbitrary path and aligns the characters, that it encircles, along this path:

<pre>&lt;path id="my_path" d="M 20,20 C 40,40 80,40 100,20" /&gt;
&lt;text&gt;
  &lt;textPath xlink:href="#my_path"&gt;This text follows a curve.&lt;/textPath&gt;
&lt;/text&gt;</pre>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Texts
|MSDN_link=
|HTML5Rocks_link=
}}