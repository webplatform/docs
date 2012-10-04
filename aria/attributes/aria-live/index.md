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
 
The '''ariaLive''' attribute indicates the priority of updates to a live region. Announcing changes immediately can be disorienting for users. Most updates should be announced only when the user is idle.
To supress notifications until after a region has finished updating, set [[aria/attributes/aria-busy|'''ariaBusy''']].
'''Note'''  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties; for example, <code>object.setAttribute("aria-valuenow", newValue)</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203793 Accessible Rich Internet Applications (WAI-ARIA) 1.0], Section 6.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[aria|Accessible Rich Internet Applications (ARIA)]]</code>
*<code>Reference</code>
*<code>[[aria/attributes/aria-busy|aria-busy]]</code>
*<code>[[aria/attributes/aria-relevant|aria-relevant]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}