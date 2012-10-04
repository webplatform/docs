{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=lIndex|Data type=Integer|Description=A zero-based index of the list entry, up to the length of the collection.|Optional=}}
|Method_applies_to=apis/web-storage/HTMLStorage
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=String


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The key can be any string, including the empty string.
The order of keys may change when items are added to the collection.
Free the memory returned in ''pbstrKey'' with '''SysFreeString'''.
This method will throw an "Invalid Argument" exception if ''lIndex'' is out of range.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196999 Web Storage], Section 4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Storage</code>
*<code>[[apis/web-storage/methods/getItem|getItem]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}