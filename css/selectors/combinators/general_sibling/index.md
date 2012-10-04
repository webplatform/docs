{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The general sibling combinator is a "tilde" (~) character that separates two simple selectors. Whitespace is not significant.
A selector of the form "E~F" matches element F when it follows sibling element E in the document tree, ignoring non-element nodes (such as text nodes and comments). Element E and F must share the same parent but does not necessarily precede F directly. To match the first child of the parent, use the [[css/selectors/pseudo-classes/:first-child|''':first-child''']] pseudo-class.
'''Note'''  Requires Windows Internet Explorer 7 or later.
'''Note'''  Combinators are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [[html/elements/!DOCTYPE|!DOCTYPE]] directive that specifies a standards-based document. For more information, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}125785 Defining Document Compatibility].
|Import_Notes=
===Syntax===
<code>''first'''''~'''''second'' { ... }
</code>
===Parameters===
;''first'':A CSS simple selector.
;''second'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 6.3


}}
{{See_Also_Section
|Topic_clusters=Selectors, Combinators
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}