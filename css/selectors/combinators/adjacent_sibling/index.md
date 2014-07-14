{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This is referred to as an adjacent selector. It will select only the element that is immediately preceded by the former element.}}
{{CSS_Selector
|Content=An adjacent sibling combinator selects an element that appears directly after a specified sibling element. It is created by placing a plus sign (+) between two simple selectors. For example [[html/elements/li|li]]  + [[html/elements/li|li]] will select a [[html/elements/li|list item]] directly following another, sibling [[html/elements/li|list item]].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=li + li {
  border-left: 1px solid #333;
}
|LiveURL=http://code.webplatform.org/gist/8928240
}}
}}
{{Notes_Section
|Notes====Remarks===
The adjacent sibling combinator is a "plus sign" (+) character that separates two simple selectors. Whitespace is not significant.
A selector of the form "E+F" matches element F when it immediately follows sibling element E in the document tree, ignoring non-element nodes (such as text nodes and comments). Element E and F must share the same parent and E must immediately precede F. To match the first child of the parent, use the :first-child pseudo-class.
'''Note'''  Requires Windows Internet Explorer 7 or later.
'''Note'''  Combinators are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [[html/elements/!DOCTYPE|!DOCTYPE]] directive that specifies a standards-based document. For more information, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}125785 Defining Document Compatibility].
|Import_Notes====Syntax===
<code>''first'''''+'''''second'' { ... }
</code>
===Parameters===
;''first'':A CSS simple selector.
;''second'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.7
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=7.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Combinators, Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}