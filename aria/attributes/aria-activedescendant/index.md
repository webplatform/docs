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
<dt>composite</dt>
<dt>group</dt>
<dt>textbox</dt>
</dl>
{{!}}}
 
To simplify keyboard navigation, an element that gains focus may specify the currently active child element by [[html/attributes/id|'''id''']].

The container element should change the designated descendant during a
[[dom/events/keypress|'''keypress''']]
event. The container should also ensure that the current child has a style that visibly shows it is active, such as an outline or different background color.
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
}}
{{Topics|ARIA}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}