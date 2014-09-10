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
 
One or more [[html/attributes/id|'''id''']] properties may be specified. A list of '''id''' properties is returned by Microsoft UI Automation.
In addition to providing the '''ariaLabelledby''' property, you should also use a '''label''' element to indicate a label for previous versions of the browser.

'''Note'''  For cross-browser compatibility, always use the WAI-ARIA attribute syntax to access and modify ARIA properties, for example <code>object.setAttribute("aria-valuenow", newValue)</code>.
If more than one [[html/attributes/id|'''id''']] is specified, only the first id is recognized by Windows Internet Explorer 8.
'''Note'''  Recursive use of '''ariaLabelledby''' is not supported. An element that is using '''ariaLabelledby''' should not reference another element that is also using '''ariaLabelledby'''.
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
*<code>Reference</code>
*<code>[[aria/attributes/aria-controls|aria-controls]]</code>
*<code>[[aria/attributes/aria-flowto|aria-flowto]]</code>
*<code>[[aria/attributes/aria-describedby|aria-describedby]]</code>
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