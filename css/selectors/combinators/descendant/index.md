{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Selects any instance of an element that is a descendant (child, grandchild and beyond) of another element.}}
{{CSS_Selector
|Content=Use a descendant combinator to select every instance of an element under its ancestor. Create a descendant combinator by adding a whitespace between two simple selectors. For example <code>nav ul</code> will target every instance of an [[html/elements/ul|unordered list]] found inside of a [[html/elements/nav|navigation]] element. 

For performance considerations, take care to not over-qualify selectors. For instance, html and body are unnecessary in the following example: <code>html body article a {}</code>. It's a given that an article will be found in the body which will be found in the html. There is no reason to require that the browser try to match any further than the article—as browsers read selectors from right to left.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following rule defines a text color of red for all instances of unordered lists within navigation elements.
|Code=nav ul { color:red; }
|LiveURL=http://code.webplatform.org/gist/8413346
}}
}}
{{Notes_Section
|Usage=
|Notes=Descendant combinators were called contextual selectors in Cascading Style Sheets, Level 1 (CSS1).

To skip over a generation of elements and pass styles to descendants beyond child elements, combine the Universal (*) Selector with the Descendant Combinator. For example, the following selector matches any '''p''' elements that are not direct descendants (grandchildren or later) of a '''div''' element.
<code>DIV * P {}</code>
|Import_Notes====Syntax===
<code>''first''''' '''''second'' { ... }
</code>
===Parameters===
;''first'':A CSS simple selector.
;''second'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 2 Specification
|URL=http://www.w3.org/TR/CSS2/
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=5+
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3+
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3+
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}