{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Needs summary, example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Applies_to=
|Property_applies_to=dom/HTMLElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
{{{!}} class="wikitable"
{{!}}-
!Used in Roles
{{!}}<dl>
<dt>No role required.</dt>
</dl>
{{!}}}
 
This property defines element relationships and associations that cannot be readily determined from the document structure.
When the
'''aria-flowto''' property contains a single
[[html/attributes/id|'''id''']] property,
the
assistive technology should resume reading at the targeted element. However, when the
'''aria-flowto''' property contains multiple
'''id''' properties,  the
assistive technology should give users the option of navigating to any targeted element.
'''Note'''  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example <code>object.setAttribute("aria-valuenow", newValue)</code>.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203793 Accessible Rich Internet Applications (WAI-ARIA) 1.0], Section 6.6
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[aria|Accessible Rich Internet Applications (ARIA)]]</code>
*<code>[[aria/attributes/x-ms-aria-flowfrom|x-ms-aria-flowfrom]]</code>
}}
{{Topics|ARIA}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}