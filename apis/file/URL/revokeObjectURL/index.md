{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=url|Data type=BSTR|Description=String that indicates the URL to revoke from the document.|Optional=}}
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=This method does not return a value.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
This method does not need to be called on a URL object that was created using [[apis/file/properties/oneTimeOnly|'''oneTimeOnly''']] set to true, providing it is used. If a URL object is created and not used, this method must be called to revoke it.  All URLs that are not revoked will be destroyed when the markup that created them is torn down.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/file/URL|URL]]</code>
*<code>[[apis/file/ObjectURLOptions|ObjectURLOptions]]</code>
*<code>[[apis/file/properties/oneTimeOnly|oneTimeOnly]]</code>
*<code>[[apis/file/methods/createObjectURL|createObjectURL]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}