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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''param''' element to specify a run-time parameter for the object specified by the '''object''' element.  A URI is specified for the Windows Media Player control.
|LiveURL=
|Code=
&lt;OBJECT CLASSID{{=}}"clsid:22D6F312-B0F6-11D0-94AB-0080C74C7E95"&gt;
&lt;PARAM NAME{{=}}"FileName" 
VALUE{{=}}"http://msdn.microsoft.com/workshop/samples/author/behaviors/media/28movie.asf"
VALUETYPE{{=}}"ref" TYPE{{=}}"video/*"/&gt;
&lt;/OBJECT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''valueType''' was introduced in Microsoft Internet Explorer 6
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>param</code>
*<code>Conceptual</code>
*<code>Binding HTML Elements to Data</code>
*<code>Introduction to Data Binding</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}