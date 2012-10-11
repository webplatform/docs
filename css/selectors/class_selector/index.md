Working with HTML, authors may use the "period" notation (also known as "full stop", U+002E, .) as an alternative to the ~= notation when representing the class attribute. Thus, for HTML, div.value and <code>div[class~=value]</code> have the same meaning. The attribute value must immediately follow the full stop (<code>.</code>).

UAs may apply selectors using the period (<code>.</code>) notation in XML documents if the UA has namespace-specific knowledge that allows it to determine which attribute is the "class" attribute for the respective namespace. One such example of namespace-specific knowledge is the prose in the specification for a particular namespace (e.g. SVG 1.0 [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#SVG11 SVG11] describes the SVG class attribute and how a UA should interpret it, and similarly MathML 1.01 [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#MATHML MATHML] describes the MathML class attribute.)

== CSS examples: ==

We can assign style information to all elements with <code>class~="pastoral"</code> as follows:

<syntaxhighlight lang="css">*.pastoral { color: green }  /* all elements with class~=pastoral */</syntaxhighlight>

or just

<syntaxhighlight lang="css">.pastoral { color: green }  /* all elements with class~=pastoral */</syntaxhighlight>

The following assigns style only to H1 elements with <code>class~="pastoral"</code>:

<syntaxhighlight lang="css">H1.pastoral { color: green }  /* H1 elements with class~=pastoral */</syntaxhighlight>

Given these rules, the first H1 instance below would not have green text, while the second would:

<syntaxhighlight lang="html5"><H1>Not green</H1>
<H1 class="pastoral">Very green</H1></syntaxhighlight>

The following rule matches any P element whose class attribute has been assigned a list of whitespace-separated values that includes both pastoral and marine:

<syntaxhighlight lang="css">p.pastoral.marine { color: green }</syntaxhighlight>

This rule matches when <code>class="pastoral blue aqua marine"</code> but does not match for <code>class="pastoral blue"</code>.

<blockquote>'''Note:''' Because CSS gives considerable power to the "class" attribute, authors could conceivably design their own "document language" based on elements with almost no associated presentation (such as DIV and SPAN in HTML) and assigning style information through the "class" attribute. Authors should avoid this practice since the structural elements of a document language often have recognized and accepted meanings and author-defined classes may not. </blockquote>

<blockquote>'''Note:''' If an element has multiple class attributes, their values must be concatenated with spaces between the values before searching for the class. As of this time the working group is not aware of any manner in which this situation can be reached, however, so this behavior is explicitly non-normative in this specification.</blockquote>
[[Category: CSS]]