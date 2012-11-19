{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Navigates to a relatively positioned history record.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=relativePosition
|Data type=Number
|Description=The relative position of a URL in the history list. Out of bounds position (-1 when the current document is the first history record) does nothing.
|Optional=No
}}
|Method_applies_to=dom/history
|Example_object_name=history
|Javascript_data_type=void
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=An error does not occur if the user tries to go beyond the beginning or end of the history. Instead, the user remains at the current page.
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
|Note=Non standard. The first parameter can also be a string that indicates an exact URL in the History list.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>history</code>
*<code>Reference</code>
*<code>back</code>
*<code>forward</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}