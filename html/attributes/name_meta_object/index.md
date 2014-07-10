{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
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
|Description=This example adds '''meta''' tags to the '''head''' of an HTML document to display a smart edit button on the toolbar as of Internet Explorer 5. Because the '''ProgID''' '''meta''' tag is associated with the programmatic identifier of Word, the button displays the Word icon. When you click the button, Internet Explorer loads the document into Word using the specified document template.
|Code=&lt;META NAME{{=}}"ProgID" CONTENT{{=}}"word.document"&gt;
&lt;META NAME{{=}}"Template" CONTENT{{=}}"C:\Program Files\Microsoft Office\Office\html.dot"&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''NAME''' attribute typically is assigned one of the preceding well-defined values, but any arbitrary value can be specified. Custom tools can be developed to perform special actions on documents containing arbitrary '''meta''' tags.
To enable the smart edit features in Microsoft Internet Explorer 5 or later, add a '''meta''' tag to the '''head''' of the document. Associate '''ProgID''' with the '''NAME''' attribute, and associate the programmatic identifier of the desired editor with the '''CONTENT''' attribute. If the specified editor is not installed or properly registered on the user's system, the edit button is not displayed. Consult the documentation of your editor to determine its programmatic identifier.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 7.4.4
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
*<code>meta</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}