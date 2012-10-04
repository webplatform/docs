{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|ARIA}}
{{Notes_Section
|Notes=
===Remarks===
{| class="wikitable"
|-
!Used in Roles
|<dl>
<dt>No role required.</dt>
</dl>
|}
 
This property applies to live regions in the user interface. If authors know that multiple parts of the same live region need to be loaded, they can set '''aria-busy''' to '''true''' when the first part is loaded, and then set it to '''false''' when the last part is loaded.
'''Note'''  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example <code>object.setAttribute("aria-valuenow", newValue)</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203793 Accessible Rich Internet Applications (WAI-ARIA) 1.0], Section 6.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[aria|Accessible Rich Internet Applications (ARIA)]]</code>
*<code>[http://go.microsoft.com/fwlink/p/?linkid{{=}}203793 W3C ARIA-Busy]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}