{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets or sets the preferred MIME name of the document's character encoding.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//displays the document's character encoding string
function showCharSet() {
    alert(document.characterSet);
}

//sets the document's character encoding string
function putCharSet() {
    document.characterSet = "windows-1252";
}

}}
}}
{{Notes_Section
|Usage=On setting, if the new value is an IANA-registered alias for a character encoding supported by the user agent, the document's character encoding is set to that character encoding. Otherwise, nothing happens.
|Notes====Remarks===
For [[html/elements/a|'''a''']],  '''link''', and '''script''' objects, you must set the value of this property before you can retrieve it.
You must set the value of this property before you can retrieve it.
In Microsoft Internet Explorer 6, This property now applies to the [[html/elements/a|'''a''']], '''link''', and '''script''' objects.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}