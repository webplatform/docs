{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Notes_Section
|Notes=
===Remarks===
A '''Submit''' button has the same default behavior as a button created by using the '''submit''' [[html/attributes/type|'''type''']] with the '''input''' object. If the ENTER key is pressed while a user is viewing a form that contains a '''Submit''' button, the form is submitted. This default behavior of a '''Submit''' button is indicated by a border surrounding the button. The border appears when any control in the form receives the focus, other than another button. If the '''Submit''' button has a [[html/attributes/name|'''name''']] property, the button contributes a name/value pair to the submitted data.
Windows Internet Explorer 8 and later. The default value of this attribute depends on the current document compatibility mode.  In IE8 Standards mode, the default value is <code>submit</code>.  In other compatibility modes and earlier versions of Windows Internet Explorer, the default value is <code>button</code>.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>button</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}