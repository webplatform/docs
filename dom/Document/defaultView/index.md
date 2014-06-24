{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=needs a better example and compat table
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the Document's browsing context's Window object (essentially the environment in which objects are presented to the user) if there is one, or null otherwise.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=No
|Example_object_name=document
|Return_value_name=Window
|Javascript_data_type=Object
|Return_value_description=Returns the Window object of the active document
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//displays the document's browsing context
function showDefView() {
    alert(document.defaultView);
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5 Specification
|URL=http://www.w3.org/TR/html5/browsers.html#window
|Status=Working Draft
}}
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
*<code>[[dom/Document|Document]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}