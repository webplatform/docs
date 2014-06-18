{{Page_Title|CSS选择器}}
{{Flags
|State=In Progress
|Checked_Out=No
}}
{{Summary_Section|A Selector represents a structure. This structure can be used as a condition (e.g. in a CSS rule) that determines which elements a selector matches in the document tree, or as a flat description of the HTML or XML fragment corresponding to that structure.

Selectors may range from simple element names to rich contextual representations.
}}
{{Basic Page}}
== CSS选择器参考 ==
=== 标签选择器 ===
*[[css/selectors/type|<code>elementname</code>]]

=== 通配符 ===
*[[css/selectors/universal_selector|<code>*</code>]]

=== [[css/selectors/attribute_selector|属性选择器]] ===
*<code>[[css/selectors/attributes/existence|[attributename]]]</code>
*<code>[[css/selectors/attributes/equality|[attributename="val"]]]</code>
*<code>[[css/selectors/attributes/whitespace|[attributename~="val"]]]</code>
*<code>[[css/selectors/attributes/hyphen|[attributename{{!}}="val"]]]</code>
*<code>[[css/selectors/attributes/prefix|[attributename^="val"]]]</code>
*<code>[[css/selectors/attributes/suffix|[attributename$="val"]]]</code>
*<code>[[css/selectors/attributes/substring|[attributename*="val"]]]</code>

=== 类选择器 ===
*[[css/selectors/class_selector|<code>.classname</code>]]

=== ID选择器 ===
*[[css/selectors/id_selector|<code>#idname</code>]]

=== 伪类 ===
==== [[css/selectors/pseudo-classes/Dynamic_pseudo-classes|Dynamic pseudo-classes]] ====
*<code>[[:css/selectors/pseudo-classes/:link|:link]]</code>
*<code>[[:css/selectors/pseudo-classes/:visited|:visited]]</code>
*<code>[[:css/selectors/pseudo-classes/:hover|:hover]]</code>
*<code>[[:css/selectors/pseudo-classes/:active|:active]]</code>
*<code>[[:css/selectors/pseudo-classes/:focus|:focus]]</code>

==== The target pseudo-class ====
*[[css/selectors/pseudo-classes/:target|<code>:target</code>]]

==== The language pseudo-class ====
*[[css/selectors/pseudo-classes/:lang|<code>:lang</code>]]

==== [[css/selectors/pseudo-classes/ui_element_states_pseudo-classes|The UI element states pseudo-classes]] ====
*<code>[[:css/selectors/pseudo-classes/:enabled|:enabled]]</code>
*<code>[[:css/selectors/pseudo-classes/:disabled|:disabled]]</code>
*<code>[[:css/selectors/pseudo-classes/:checked|:checked]]</code>

==== [[css/selectors/pseudo-classes/Structural_pseudo-classes|Structural pseudo-classes]] ====
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:root_pseudo-class|<code>:root</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-child.28.29_pseudo-class|<code>:nth-child</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-last-child.28.29_pseudo-class|<code>:nth-last-child</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-of-type.28.29_pseudo-class|<code>:nth-of-type</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-last-of-type.28.29_pseudo-class|<code>:nth-last-of-type</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:first-child_pseudo-class|<code>:first-child</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:last-child_pseudo-class|<code>:last-child</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:first-of-type_pseudo-class|<code>:first-of-type</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:last-of-type_pseudo-class|<code>:last-of-type</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:only-child_pseudo-class|<code>:only-child</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:only-of-type_pseudo-class|<code>:only-of-type</code>]]
*[[css/selectors/pseudo-classes/Structural_pseudo-classes#:empty_pseudo-class|<code>:empty</code>]]

==== The negation pseudo-class ====
*[[css/selectors/pseudo-classes/:not|<code>:not</code>]]

=== Pseudo-elements ===
*[[:css/selectors/pseudo-elements/::first-line|<code><span>:</span>:first-line</code>]]
*[[:css/selectors/pseudo-elements/::first-letter|<code><span>:</span>:first-letter</code>]]
*[[:css/selectors/pseudo-elements/::before|<code><span>:</span>:before</code>]]
*[[:css/selectors/pseudo-elements/::after|<code><span>:</span>:after</code>]]

=== Combinators ===
==== Descendant combinator ====
*[[css/selectors/combinators/descendant|<code>A B</code>]]

==== Child combinator ====
*[[css/selectors/combinators/child|<code>A > B</code>]]

==== Adjacent sibling combinator ====
*[[css/selectors/combinators/adjacent_sibling|<code>A + B</code>]]

==== General sibling combinator ====
*[[css/selectors/combinators/general_sibling|<code>A ~ B</code>]]

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

In this example, we condense three rules with identical declarations into one. Thus,
<syntaxhighlight lang="css">
h1 { font-family: sans-serif }
h2 { font-family: sans-serif }
h3 { font-family: sans-serif }
</syntaxhighlight>
is equivalent to:

<syntaxhighlight lang="css">
h1, h2, h3 { font-family: sans-serif }
</syntaxhighlight>

'''Warning''': the equivalence is true in this example because all the selectors are valid selectors. If just one of these selectors were invalid, the entire group of selectors would be invalid. This would invalidate the rule for all three heading elements, whereas in the former case only one of the three individual heading rules would be invalidated. 

Invalid CSS example:
<syntaxhighlight lang="css">
h1 { font-family: sans-serif }
h2..foo { font-family: sans-serif }
h3 { font-family: sans-serif }
</syntaxhighlight>
is not equivalent to:
<syntaxhighlight lang="css">
h1, h2..foo, h3 { font-family: sans-serif }
</syntaxhighlight>
because the above selector (h1, h2..foo, h3) is entirely invalid and the entire style rule is dropped. (When the selectors are not grouped, only the rule for h2..foo is dropped.)


== See also ==
*[http://www.w3.org/TR/css3-selectors/ Selectors Level 3 Specification]
*[[tutorials/using_selectors|Using Selectors Tutorial]]
*[[css/tutorials|CSS Educational Materials for Beginners]]
*[[css/properties|CSS Properties Reference]]

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