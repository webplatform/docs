{{Page Title}}
{{Flags
|State=Not Ready
|Editorial notes=summary, examples best practices, compatibility, standards, clean-up of MSDN sections
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example retrieves the '''frame''' element of the window and sets its source URL to Microsoft Developer Network (MSDN) Online.
|LiveURL=
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
    var oFrame {{=}} window.frameElement;
    oFrame.src {{=}} "http://msdn.microsoft.com";
&lt;/SCRIPT&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
The window must be a '''frame''' or '''iframe'''.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}