{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  Requires Windows Internet Explorer 7 or later.
'''Note'''  Attribute selectors are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [[html/elements/!DOCTYPE|!DOCTYPE]] directive that specifies a standards-based document. For more information, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}125785 Defining Document Compatibility].
Attributes are case-sensitive. Matches any E element whose "att" attribute value is a list of space-separated values, one of which is exactly equal to "val".
If the target ''val'' contains whitespace, the rule will not match anything.
|Import_Notes====Syntax===
<code>
E[''att'''''~{{=}}'''''val'']
{...}</code>
===Parameters===
;''att'':Must be either an Identifier or a String.
;''val'':Must be either an Identifier or a String.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Attribute selectors
|URL=http://www.w3.org/TR/CSS2/selector.html#attribute-selectors
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
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