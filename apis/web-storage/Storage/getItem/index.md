{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrKey|Data type=BSTR|Description=The name of the key (a valid UTF-16 string, including the empty string).|Optional=}}
|Method_applies_to=apis/web-storage/HTMLStorage
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Variant

bstrKey


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Any valid UTF-16 string, including the empty string, is a valid key name.
If the specified ''bstrKey'' does not exist in the list associated with the object, then this method returns '''null'''.
Attempts to read or write a secured item from script running in the context of an unsecured URL are not permitted.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196999 Web Storage], Section 4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Storage</code>
*<code>[[apis/web-storage/methods/setItem|setItem]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}