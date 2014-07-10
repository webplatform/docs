{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Merge_Candidate
|Other=[[html/attributes/type]]
}}
|Checked_Out=No
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''param''' element to specify a run-time parameter for the object specified by the '''object''' element.  A URI is specified for the Windows Media Player control.
|Code=&lt;OBJECT CLASSID{{=}}"clsid:22D6F312-B0F6-11D0-94AB-0080C74C7E95"&gt;
&lt;PARAM NAME{{=}}"FileName" 
VALUE{{=}}"http://msdn.microsoft.com/workshop/samples/author/behaviors/media/28movie.asf"
VALUETYPE{{=}}"ref" TYPE{{=}}"video/*"/&gt;
&lt;/OBJECT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The content type specifies the nature of a linked resource.  Examples of content types include "text/html", "image/png", "image/gif", "video/mpeg", "audio/basic", "text/tcl", "text/javascript", and "text/vbscript". For the current list of registered content types, see [http://go.microsoft.com/fwlink/p/?linkid{{=}}203647 MIME Media Types].
'''type''' was introduced in Microsoft Internet Explorer 6
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
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
*<code>param</code>
*<code>Conceptual</code>
*<code>Binding HTML Elements to Data</code>
*<code>Introduction to Data Binding</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}