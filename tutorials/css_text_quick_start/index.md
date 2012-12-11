{{Page_Title|CSS text quick start}}
{{Flags}}
{{Byline}}
{{Summary_Section|This tutorial provides a quick instruction on styling text with CSS.}}
{{Tutorial
|Content=== Information on text styles ==
 
CSS has several properties for styling text.
 
There is a convenient shorthand property, [font], which you can use to specify several aspects at once—for example:
 
* Bold, italic, and small-caps (small capital letters)
* The size
* The line height
* The font typeface
  
Consider this example:

<syntaxhighlight lang="css">p {font: italic 75%/125% "Comic Sans MS", cursive;}</syntaxhighlight>
 
<p style="font: italic 75%/125% "Comic Sans MS", cursive;">This rule sets various font properties, making all paragraphs italic.</p>

* The font size is set to three-quarters of the size in each paragraph's parent element, and the line height is set to 125% (spaced a little wider than normal).
* The font typeface is set to Comic Sans MS, but if this typeface is not available, then the browser will use its default cursive (hand-written) typeface.

 The rule has the side-effect of turning off of bold and small-caps (setting them to <code>normal</code>):
 
=== Font faces ===
 
You cannot predict what typefaces visitors of your site will have. So when you specify font typefaces, it is a good idea to give a list of alternatives in order of preference. End the list with one of the built-in default typefaces: <code>serif</code>, <code>sans-serif</code>, <code>cursive</code>, <code>fantasy</code> or <code>monospace</code>.

If the typeface does not support some features in the document, then the browser can substitute a different typeface. For example, the document might contain special characters that the typeface does not support. If the browser can find another typeface that has those characters, then it will use the other typeface.

To specify a typeface on its own, use the [font-family] property.

=== Font sizes ===
 
Browser users can override the default font sizes or change the text size while they read a page, so it makes good sense for you to use relative sizes wherever you can.

You can use some built-in values for font sizes, like <code>small</code>, <code>medium</code> and <code>large</code>. You can also use values relative to the font size of the parent element, like: <code>smaller</code>, <code>larger</code>, <code>150%</code> or <code>1.5em</code>. An "em" is equivalent to the width of the letter "m" (for the font size of the parent element); thus 1.5em is one-and-a-half times the size of the font of the parent element.

If necessary, you can specify an actual size, like this: <code>14px</code> (14 pixels) for a display device or 14pt (14 points) for a printer. This practice does not promote accessibility for visually impaired users, because it does not allow them to change the size of text characters. A more accessible strategy is to set a built-in value like medium on a top-level element of the document, and then set relative sizes for all its descendent elements.

To specify a font size on its own, use the [font-size] property.
 
=== Line height ===
 
The line height property specifies the spacing between lines. If your document has long paragraphs that contain many lines, a larger-than-normal spacing value makes text easier to read, especially if the font size is small.
 
To specify a line height on its own, use the [line-height] property.

 
=== Decoration ===
 
The separate [text-decoration] property can specify other styles, like <code>underline</code> or <code>line-through</code>. You can set it to <code>none</code> to explicitly remove any decoration.
 
=== Other properties ===
 
To specify italic on its own, use <code>[font-style]: italic;</code><br>
To specify bold on its own, use <code>[font-weight]: bold;</code><br>
To specify small capitalized letters on its own, use <code>[font-variant]: small-caps;</code>
 
To turn any of these off individually, you can specify the value <code>normal</code> or <code>inherit</code>.
  
==More details on applying text styles==

You can specify text styles in a variety of other ways. For example, some of the properties mentioned here have other values that you can use. In a complex style sheet, avoid using the shorthand <code>font</code> property, because of its side-effects (resetting other individual properties).

For full details of the properties that relate to fonts, see [http://www.w3.org/TR/CSS21/fonts.html Fonts] in the CSS Specification. For full details of text decoration, see [http://www.w3.org/TR/css3-text/ Text] there. If you do not want to depend on the typefaces installed on visitors' systems, you can use [[@font-face]] to specify an online font. However, this requires that the visitors are using a browser that supports this rule.

== Action: Specifying fonts ==
 
For a simple document, you can set the font of the <code>&lt;body&gt;</code> element and the rest of the document inherits the settings.

<ol>
<li><p>Edit your CSS file.</p></li>
<li><p>Add the following rule to change the font throughout the document. The top of the CSS file is a logical place for it, but it has the same effect wherever you put it:</p>
<syntaxhighlight lang="css">body {font: 16px "Comic Sans MS", cursive;}</syntaxhighlight></li>
<li><p>Add a comment explaining the rule, and add white space to make it match your preferred layout.</p></li>
<li><p>Save the file and refresh your browser to see the effect. If your system has Comic Sans MS, or another cursive font that does not support italic, then your browser chooses a different font face for the italic text in the first line.</p>
<p class="note">Include screenshot to show what it should look like.</p></li>
<li><p>From your browser's menu bar, choose '''View &gt; Text Size &gt; Increase''' (or '''View &gt; Zoom &gt; Zoom In'''). Even though you specified 16 pixels in the CSS style, a visitor reading the page can change the size of the text.</p></li>
</ol>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Exercise questions===
 
Without changing anything else, make all six initial letters twice the size in the browser's default serif font.
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Text_styles
|MSDN_link=
|HTML5Rocks_link=
}}