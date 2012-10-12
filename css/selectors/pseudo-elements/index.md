Pseudo-elements create abstractions about the document tree beyond those specified by the document language. For instance, document languages do not offer mechanisms to access the first letter or first line of an element's content. Pseudo-elements allow authors to refer to this otherwise inaccessible information. Pseudo-elements may also provide authors a way to refer to content that does not exist in the source document (e.g., the <code>::before</code> and <code>::after</code> pseudo-elements give access to generated content).

A pseudo-element is made of two colons (<code>::</code>) followed by the name of the pseudo-element.

This <code>::</code> notation is introduced by the current document in order to establish a discrimination between pseudo-classes and pseudo-elements. For compatibility with existing style sheets, user agents must also accept the previous one-colon notation for pseudo-elements introduced in CSS levels 1 and 2 (namely, <code>:first-line</code>, <code>:first-letter</code>, <code>:before</code> and <code>:after</code>). This compatibility is not allowed for the new pseudo-elements introduced in this specification.

Only one pseudo-element may appear per selector, and if present it must appear after the sequence of simple selectors that represents the [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#subject subjects] of the selector.
<blockquote>'''Note:''' A future version of this specification may allow multiple pseudo-elements per selector.</blockquote>

==The <code>::first-line</code> pseudo-element==
The <code>::first-line</code> pseudo-element describes the contents of the first formatted line of an element. 

CSS example:
<syntaxhighlight lang="css">
p::first-line { text-transform: uppercase }
</syntaxhighlight>
The above rule means "change the letters of the first line of every p element to uppercase". The selector <code>p::first-line</code> does not match any real document element. It does match a pseudo-element that conforming user agents will insert at the beginning of every <code>p</code> element.

Note that the length of the first line depends on a number of factors, including the width of the page, the font size, etc. Thus, an ordinary HTML paragraph such as:
<syntaxhighlight lang="html5">
<P>This is a somewhat long HTML 
paragraph that will be broken into several 
lines. The first line will be identified
by a fictional tag sequence. The other lines 
will be treated as ordinary lines in the 
paragraph.</P>
</syntaxhighlight>
the lines of which happen to be broken as follows:
<syntaxhighlight lang="html5">
THIS IS A SOMEWHAT LONG HTML PARAGRAPH THAT
will be broken into several lines. The first
line will be identified by a fictional tag 
sequence. The other lines will be treated as 
ordinary lines in the paragraph.
</syntaxhighlight>
This paragraph might be "rewritten" by user agents to include the fictional tag sequence for <code>::first-line</code>. This fictional tag sequence helps to show how properties are inherited.
<syntaxhighlight lang="html5">
<P><P::first-line> This is a somewhat long HTML 
paragraph that </P::first-line> will be broken into several
lines. The first line will be identified 
by a fictional tag sequence. The other lines 
will be treated as ordinary lines in the 
paragraph.</P>
</syntaxhighlight>
If a pseudo-element breaks up a real element, the desired effect can often be described by a fictional tag sequence that closes and then re-opens the element. Thus, if we mark up the previous paragraph with a span element:
<syntaxhighlight lang="html5">
<P><SPAN class="test"> This is a somewhat long HTML
paragraph that will be broken into several
lines.</SPAN> The first line will be identified
by a fictional tag sequence. The other lines 
will be treated as ordinary lines in the 
paragraph.</P>
</syntaxhighlight>
the user agent could simulate start and end tags for span when inserting the fictional tag sequence for <code>::first-line</code>.
<syntaxhighlight lang="html5">
<P><P::first-line><SPAN class="test"> This is a
somewhat long HTML
paragraph that will </SPAN></P::first-line><SPAN class="test"> be
broken into several
lines.</SPAN> The first line will be identified
by a fictional tag sequence. The other lines
will be treated as ordinary lines in the 
paragraph.</P>
</syntaxhighlight>

===First formatted line definition in CSS===
In CSS, the <code>::first-line</code> pseudo-element can only have an effect when attached to a block-like container such as a block box, inline-block, table-caption, or table-cell.

The first formatted line of an element may occur inside a block-level descendant in the same flow (i.e., a block-level descendant that is not out-of-flow due to floating or positioning). For example, the first line of the <code>DIV</code> in <code><DIV><P>This line...</P></DIV></code> is the first line of the <code>P</code> (assuming that both <code>P</code> and <code>DIV</code> are block-level).

The first line of a table-cell or inline-block cannot be the first formatted line of an ancestor element. Thus, in <code><DIV><P STYLE="display: inline-block">Hello<BR>Goodbye</P> etcetera</DIV></code> the first formatted line of the <code>DIV</code> is not the line "Hello".

<blockquote>'''Note:''' Note that the first line of the <code>p</code> in this fragment: <pre><p><br>First...</pre> doesn't contain any letters (assuming the default style for br in HTML 4). The word "First" is not on the first formatted line. </blockquote>

A UA should act as if the fictional start tags of the <code>::first-line</code> pseudo-elements were nested just inside the innermost enclosing block-level element. (Since CSS1 and CSS2 were silent on this case, authors should not rely on this behavior.) For example, the fictional tag sequence for
<syntaxhighlight lang="html5">
<DIV>
  <P>First paragraph</P>
  <P>Second paragraph</P>
</DIV>
</syntaxhighlight>

is
<syntaxhighlight lang="html5">
<DIV>
  <P><DIV::first-line><P::first-line>First paragraph</P::first-line></DIV::first-line></P>
  <P><P::first-line>Second paragraph</P::first-line></P>
</DIV>
</syntaxhighlight>

The <code>::first-line</code> pseudo-element is similar to an inline-level element, but with certain restrictions. The following CSS properties apply to a <code>::first-line</code> pseudo-element: font properties, color property, background properties, ‘<code>word-spacing</code>’, ‘<code>letter-spacing</code>’, ‘<code>text-decoration</code>’, ‘<code>vertical-align</code>’, ‘<code>text-transform</code>’, ‘<code>line-height</code>’. UAs may apply other properties as well.

During CSS inheritance, the portion of a child element that occurs on the first line only inherits properties applicable to the <code>::first-line</code> pseudo-element from the <code>::first-line</code> pseudo-element. For all other properties inheritence is from the non-pseudo-element parent of the first line pseudo element. (The portion of a child element that does not occur on the first line always inherits from the parent of that child.)

== The <code>::first-letter</code> pseudo-element ==
The <code>::first-letter</code> pseudo-element represents the first letter of an element, if it is not preceded by any other content (such as images or inline tables) on its line. The <code>::first-letter</code> pseudo-element may be used for "initial caps" and "drop caps", which are common typographical effects.

Punctuation (i.e, characters defined in Unicode in the "open" (Ps), "close" (Pe), "initial" (Pi). "final" (Pf) and "other" (Po) punctuation classes), that precedes or follows the first letter should be included. [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#UNICODE UNICODE]

The <code>::first-letter</code> also applies if the first letter is in fact a digit, e.g., the "6" in "67 million dollars is a lot of money."

<blockquote>'''Note:''' In some cases the <code>::first-letter</code> pseudo-element should include more than just the first non-punctuation character on a line. For example, combining characters must be kept with their base character. Additionally, some languages may have specific rules about how to treat certain letter combinations. The UA definition of <code>::first-letter</code> should include at least the default grapheme cluster as defined by UAX29 and may include more than that as appropriate. In Dutch, for example, if the letter combination "ij" appears at the beginning of an element, both letters should be considered within the <code>::first-letter</code> pseudo-element. [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#UAX29 UAX29]</blockquote>

If the letters that would form the ::first-letter are not in the same element, such as "‘T" in <pre><p>'<em>T...</pre>, the UA may create a <code>::first-letter</code> pseudo-element from one of the elements, both elements, or simply not create a pseudo-element.

Similarly, if the first letter(s) of the block are not at the start of the line (for example due to bidirectional reordering), then the UA need not create the pseudo-element(s).

The following CSS and HTML example illustrates how overlapping pseudo-elements may interact. The first letter of each P element will be green with a font size of ’<code>24pt</code>'. The rest of the first formatted line will be ‘<code>blue</code>’ while the rest of the paragraph will be ‘<code>red</code>’.
<syntaxhighlight lang="css">
p { color: red; font-size: 12pt }
p::first-letter { color: green; font-size: 200% }
p::first-line { color: blue }
</syntaxhighlight>
<syntaxhighlight lang="html5">
<P>Some text that ends up on two lines</P>
</syntaxhighlight>
Assuming that a line break will occur before the word "ends", the fictional tag sequence for this fragment might be:
<syntaxhighlight lang="html5">
<P>
<P::first-line>
<P::first-letter> 
S 
</P::first-letter>ome text that 
</P::first-line> 
ends up on two lines 
</P>
</syntaxhighlight>
Note that the <code>::first-letter</code> element is inside the <code>::first-line</code> element. Properties set on <code>::first-line</code> are inherited by <code>::first-letter</code>, but are overridden if the same property is set on <code>::first-letter</code>.

The first letter must occur on the first formatted line. For example, in this HTML fragment: <pre><p><br>First...</pre> the first line doesn't contain any letters and <code>::first-letter</code> doesn't match anything (assuming the default style for br in HTML 4). In particular, it does not match the "F" of "First."

[[Category:CSS]]