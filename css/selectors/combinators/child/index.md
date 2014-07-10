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
{{Summary_Section|Selects only the immediate child of a parent element.}}
{{CSS_Selector
|Content=Use a child combinator to select the direct children of a parent ancestor. Create a child combinator by placing a "greater-than sign" (&gt;) between two simple selectors. For example "ol &gt; li" will target every [[html/elements/li|list item]] element that is a direct child of an [[html/elements/ol|ordered list]] element. It will not match any further than the child in the document tree. For instance, if there were an [[html/elements/ul|unordered list]] nested inside an [[html/elements/ol|ordered list]] the [[html/elements/li|list items]] in the unordered list would not be matched.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following rule defines the text color of list item elements which are direct children of an ordered list red.
|Code=ol li {color: red;}
|LiveURL=http://code.webplatform.org/gist/8413346
}}
}}
{{Notes_Section
|Notes====Remarks===
A child combinator is a "greater-than sign" (&gt;) character that separates two simple selectors. Whitespace is not significant. A selector of the form "E&gt;F" matches when element F is a direct descendant of element E.
'''Note'''  Requires Windows Internet Explorer 7 or later.
'''Note'''  Combinators are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [[html/elements/!DOCTYPE|!DOCTYPE]] directive that specifies a standards-based document. For more information, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}125785 Defining Document Compatibility].
|Import_Notes====Syntax===
<code>''first'''''&gt;'''''second'' { ... }
</code>
===Parameters===
;''first'':A CSS simple selector.
;''second'':A CSS simple selector.
===Standards information===
*[http://www.w3.org/TR/CSS21/selector.html#child-selectors CSS 2.1], Section 5.6
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
|Internet_explorer_version=7+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/aa358819%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}