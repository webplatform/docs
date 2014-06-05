{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
{| class="wikitable"
|-
!Used in Roles
|<dl>
<dt>No role required.</dt>
</dl>
|}
 
This property defines element relationships and associations that cannot be readily determined from the document structure.
The
'''aria-controls''' property is used primarily by elements where the
[[html/attributes/role|'''role''']] property value is <code>group</code>, <code>region</code>, or <code>widget</code>. Compare this usage with that of the
[[aria/attributes/aria-owns|'''aria-owns''']] property.
'''Note'''  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example <code>object.setAttribute("aria-valuenow", newValue)</code>.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203793 Accessible Rich Internet Applications (WAI-ARIA) 1.0], Section 6.6
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
|Manual_sections====Related pages (MSDN)===
*<code>[[aria|Accessible Rich Internet Applications (ARIA)]]</code>
*<code>Reference</code>
*<code>[[aria/attributes/aria-describedby|aria-describedby]]</code>
*<code>[[aria/attributes/aria-flowto|aria-flowto]]</code>
*<code>[[aria/attributes/aria-labelledby|aria-labelledby]]</code>
*<code>[[aria/attributes/aria-owns|aria-owns]]</code>
*<code>[[aria/attributes/aria-posinset|aria-posinset]]</code>
*<code>[[aria/attributes/aria-setsize|aria-setsize]]</code>
}}
{{Topics|Accessibility, ARIA}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}