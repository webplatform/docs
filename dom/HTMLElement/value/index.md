{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8 or later. In IE8 Standards mode, the '''value''' property is correctly reported as a canonical attribute name. For example, <code>&lt;input type{{=}}"text" readonly&gt;</code> and <code>&lt;input type{{=}}"text" readonly{{=}}"readonly"&gt;</code> would both set the input text field to read-only. In IE8 mode, the value is evaluated as a canonical value, <code>"readonly"</code>. In earlier document compatibility modes, it is evaluated as a Boolean value, true. For more information, see Attribute Differences in Internet Explorer 8.
'''value''' was introduced in Microsoft Internet Explorer 6.
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
*<code>[[dom/Node/attributes|attributes]]</code>
*<code>[[dom/Node/nodeValue|nodeValue]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}