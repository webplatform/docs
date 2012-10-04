{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
This function returns an S_OK even if the element is not found. The programmer should check the value of the ''ppHTMLStyleSheetRule'' pointer returned by this call. If the value of the pointer is NULL, the element was not found and the call was not successful.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Parameters===
;''index'' [in]:Type: '''Integer''' '''<b>Integer''' that specifies the zero-based index of the object to retrieve.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/rules|rules]]</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}