{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves a list of elements that describe the current object.}}
{{Markup_Attribute
|Applies_to=
|Property_applies_to=dom/HTMLElement
|Content====Syntax===
<syntaxhighlight lang="html5">
<element aria-describedby="p" ...>
</syntaxhighlight>

===Property values===
Type: String 

A space-separated list of id property values.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=This property defines element relationships and associations that cannot be readily determined from the document structure.
The
'''aria-describedby''' property is intended to provide additional information which some users might need, and supplements the basic information provided by
'''label'''.
If more than one
[[html/attributes/id|'''id''']] property is specified, all elements are combined together to create a single description. 

'''Note'''  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example <code>object.setAttribute("aria-valuenow", newValue)</code>.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203793 Accessible Rich Internet Applications (WAI-ARIA) 1.0], Section 6.6
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages===
*<code>[[aria|Accessible Rich Internet Applications (ARIA)]]</code>
*<code>Reference</code>
*<code>[[aria/attributes/aria-controls|aria-controls]]</code>
*<code>[[aria/attributes/aria-flowto|aria-flowto]]</code>
*<code>[[aria/attributes/aria-labelledby|aria-labelledby]]</code>
*<code>[[aria/attributes/aria-owns|aria-owns]]</code>
*<code>[[aria/attributes/aria-posinset|aria-posinset]]</code>
*<code>[[aria/attributes/aria-setsize|aria-setsize]]</code>
}}
{{Topics|ARIA}}
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}