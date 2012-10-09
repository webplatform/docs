{{Page_Title|CSS selectors}}
{{Flags
|Content=Cleanup, Broken Links
}}
{{Summary_Section|A Selector represents a structure. This structure can be used as a condition (e.g. in a CSS rule) that determines which elements a selector matches in the document tree, or as a flat description of the HTML or XML fragment corresponding to that structure.

Selectors may range from simple element names to rich contextual representations.
}}
{{Basic Page}}
== CSS Selector Reference ==
=== Type Selector ===
*[[CSS/Selectors/type_selector|elementname]]

=== Universal Selector ===
*[[CSS/Selectors/universal_selector|*]]

=== [[CSS/Selectors/attribute_selector|Attribute Selector]] ===
*attributename
*attributename="val"
*attributename~="val"
*attributename|="val"
*attributename^="val"
*attributename$="val"
*attributename*="val"

=== Class Selector ===
*[[CSS/Selectors/class_selector|.classname]]

=== ID Selector ===
*[[CSS/Selectors/id_selector|#idname]]

=== Pseudo-classes ===
==== Dynamic pseudo-classes ====
*[[CSS/Selectors/pseudo-classes/:link|:link]]
*[[CSS/Selectors/pseudo-classes/:visited|:visited]]
*[[CSS/Selectors/pseudo-classes/:hover|:hover]]
*[[CSS/Selectors/pseudo-classes/:active|:active]]
*[[CSS/Selectors/pseudo-classes/:focus|:focus]]

==== The target pseudo-class ====
*[[CSS/Selectors/pseudo-classes/:target|:target]]

==== The language pseudo-class ====
*[[CSS/Selectors/pseudo-classes/:lang|:lang]]

==== The UI element states pseudo-classes ====
*[[CSS/Selectors/pseudo-classes/:enabled|:enabled]]
*[[CSS/Selectors/pseudo-classes/:disabled|:disabled]]
*[[CSS/Selectors/pseudo-classes/:checked|:checked]]

==== Structural pseudo-classes ====
*[[CSS/Selectors/pseudo-classes/:root|:root]]
*[[CSS/Selectors/pseudo-classes/:nth-child|:nth-child]]
*[[CSS/Selectors/pseudo-classes/:nth-last-child|:nth-last-child]]
*[[CSS/Selectors/pseudo-classes/:nth-of-type|:nth-of-type]]
*[[CSS/Selectors/pseudo-classes/:nth-last-of-type|:nth-last-of-type]]
*[[CSS/Selectors/pseudo-classes/:first-child|:first-child]]
*[[CSS/Selectors/pseudo-classes/:last-child|:last-child]]
*[[CSS/Selectors/pseudo-classes/:first-of-type|:first-of-type]]
*[[CSS/Selectors/pseudo-classes/:last-of-type|:last-of-type]]
*[[CSS/Selectors/pseudo-classes/:only-child|:only-child]]
*[[CSS/Selectors/pseudo-classes/:only-of-type|:only-of-type]]
*[[CSS/Selectors/pseudo-classes/:empty|:empty]]

==== The negation pseudo-class ====
*[[CSS/Selectors/pseudo-classes/:not|:not]]

=== Pseudo-elements ===
*[[CSS/Selectors/pseudo-elements/:first-line|<span>:</span>:first-line]]
*[[CSS/Selectors/pseudo-elements/:first-letter|<span>:</span>:first-letter]]
*[[CSS/Selectors/pseudo-elements/:before|<span>:</span>:before]]
*[[CSS/Selectors/pseudo-elements/:after|<span>:</span>:after]]

=== Combinators ===
==== Descendant combinator ====
*[[CSS/Selectors/combinators/descendant|A B]]

==== Child combinator ====
*[[CSS/Selectors/combinators/child|A > B]]

==== Adjacent sibling combinator ====
*[[CSS/Selectors/combinators/adjacent|A + B]]

==== General sibling combinator ====
*[[CSS/Selectors/combinators/general|A ~ B]]

== Case sensitivity ==
All Selectors syntax is case-insensitive within the ASCII range (i.e. [a-z] and [A-Z] are equivalent), except for parts that are not under the control of Selectors. The case sensitivity of document language element names, attribute names, and attribute values in selectors depends on the document language. For example, in HTML, element names are case-insensitive, but in XML, they are case-sensitive. Case sensitivity of namespace prefixes is defined in [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS3NAMESPACE CSS3NAMESPACE]. 

== Selector syntax ==
A selector is a chain of one or more sequences of simple selectors separated by combinators. One pseudo-element may be appended to the last sequence of simple selectors in a selector.
A sequence of simple selectors is a chain of simple selectors that are not separated by a combinator. It always begins with a type selector or a universal selector. No other type selector or universal selector is allowed in the sequence.

A simple selector is either a type selector, universal selector, attribute selector, class selector, ID selector, or pseudo-class.

Combinators are: whitespace, "greater-than sign" (U+003E, >), "plus sign" (U+002B, +) and "tilde" (U+007E, ~). White space may appear between a combinator and the simple selectors around it. Only the characters "space" (U+0020), "tab" (U+0009), "line feed" (U+000A), "carriage return" (U+000D), and "form feed" (U+000C) can occur in whitespace. Other space-like characters, such as "em-space" (U+2003) and "ideographic space" (U+3000), are never part of whitespace.

The elements of a document tree that are represented by a selector are the subjects of the selector. A selector consisting of a single sequence of simple selectors represents any element satisfying its requirements. Prepending another sequence of simple selectors and a combinator to a sequence imposes additional matching constraints, so the subjects of a selector are always a subset of the elements represented by the last sequence of simple selectors.

An empty selector, containing no sequence of simple selectors and no pseudo-element, is an invalid selector.
Characters in Selectors can be escaped with a backslash according to the same escaping rules as CSS. [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS21 CSS21].

Certain selectors support namespace prefixes. The mechanism by which namespace prefixes are declared should be specified by the language that uses Selectors. If the language does not specify a namespace prefix declaration mechanism, then no prefixes are declared. In CSS, namespace prefixes are declared with the @namespace rule. [http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS3NAMESPACE CSS3NAMESPACE]

== Groups of selectors ==
A comma-separated list of selectors represents the union of all elements selected by each of the individual selectors in the list. (A comma is U+002C.) For example, in CSS when several selectors share the same declarations, they may be grouped into a comma-separated list. White space may appear before and/or after the comma.

<code><pre>
CSS example:

In this example, we condense three rules with identical declarations into one. Thus,

h1 { font-family: sans-serif }
h2 { font-family: sans-serif }
h3 { font-family: sans-serif }

is equivalent to:

h1, h2, h3 { font-family: sans-serif }
</pre></code>

'''Warning''': the equivalence is true in this example because all the selectors are valid selectors. If just one of these selectors were invalid, the entire group of selectors would be invalid. This would invalidate the rule for all three heading elements, whereas in the former case only one of the three individual heading rules would be invalidated. 

<code><pre>
Invalid CSS example:

h1 { font-family: sans-serif }
h2..foo { font-family: sans-serif }
h3 { font-family: sans-serif }

is not equivalent to:

h1, h2..foo, h3 { font-family: sans-serif }

because the above selector (h1, h2..foo, h3) is entirely invalid and the entire style rule is dropped. (When the selectors are not grouped, only the rule for h2..foo is dropped.)
</pre></code>

== See also ==
*[http://www.w3.org/TR/css3-selectors/ Selectors Level 3 Specification]
*[[CSS/Training|CSS Educational Materials for Beginners]]
*[[CSS/Properties|CSS Properties Reference]]

[[Category:CSS]]


{{Special:PrefixIndex/css/selectors/}}
{{Notes_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}