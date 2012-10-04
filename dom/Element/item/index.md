{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=index|Data type=Integer|Description=An '''Integer''' that specifies the zero-based index of the object to get.|Optional=}}
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLElement'''


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''   if given a string that is not a numeric index, this method will return the object at index <code>0</code>.
This method returns S_OK, even if the element is not found. Check the value of the IDispatch pointer returned by this call. If the value of the pointer is NULL; the element was not found, and the call was not successful.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/controlRange|controlRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}