{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the status of the script.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Using the attribute at design time can improve the download performance of a document because the client does not need to parse and execute the script and can continue downloading and parsing the document instead.
|Import_Notes====Issues===
IE<10 may interleave execution of scripts. [https://github.com/h5bp/lazyweb-requests/issues/42 Discussion on Github.]

Combining scrips both standard and with <code>defer</code> that depend on each other. [https://github.com/zenorocha/browser-diet/issues/95#issuecomment-14852531 Discussion on Github.]
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=< 10
|Note=Deferral order not obeyed
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>script</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}