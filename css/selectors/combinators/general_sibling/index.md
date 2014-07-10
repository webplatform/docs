{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|A general sibling combinator selects instances of an element appearing anywhere after another element within the same parent.}}
{{CSS_Selector
|Content=A general sibling combinator selects instances of an element appearing anywhere after another sibling element. It's created by placing a tilde (~) between two simple selectors. For example <code>p ~ span</code> will select every [[html/elements/span|span]] following a [[html/elements/p|paragraph]] as long as they are found within the same parent element. Unlike the [[css/selectors/combinators/adjacent_sibling|adjacent sibling combinator]], the selected element can appear anywhere after the first element as long as they share the same parent element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=p ~ span {
	color: red;
}
|LiveURL=http://code.webplatform.org/gist/5143916
}}
}}
{{Notes_Section
|Notes====Remarks===
The general sibling combinator is a "tilde" (~) character that separates two simple selectors. Whitespace is not significant.
A selector of the form "E~F" matches element F when it follows sibling element E in the document tree, ignoring non-element nodes (such as text nodes and comments). Element E and F must share the same parent but E does not necessarily precede F directly. To match the first child of the parent, use the [[css/selectors/pseudo-classes/:first-child|''':first-child''']] pseudo-class.
'''Note'''  Requires Windows Internet Explorer 7 or later.
'''Note'''  Combinators are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [[html/elements/!DOCTYPE|!DOCTYPE]] directive that specifies a standards-based document. For more information, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}125785 Defining Document Compatibility].
|Import_Notes====Syntax===
<code>''first'''''~'''''second'' { ... }
</code>
===Parameters===
;''first'':A CSS simple selector.
;''second'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 6.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Combinators, Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/General_sibling_selectors
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}