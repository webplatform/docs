{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Revokes a URL from a document and frees the object associated with that URL.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=objectURL
|Data type=String
|Description=String that indicates the URL to revoke from the document.
|Optional=No
}}
|Method_applies_to=apis/file/URL
|Example_object_name=URL
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=This method does not need to be called on a URL object that was created using [[apis/file/properties/oneTimeOnly|'''oneTimeOnly''']] set to true, providing it is used. If a URL object is created and not used, this method must be called to revoke it.  All URLs that are not revoked will be destroyed when the markup that created them is torn down.
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
|Manual_sections=*<code>[[apis/file/ObjectURLOptions|ObjectURLOptions]]</code>
*<code>[[apis/file/properties/oneTimeOnly|oneTimeOnly]]</code>
*<code>[[apis/file/methods/createObjectURL|createObjectURL]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}