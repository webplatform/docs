{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLTableElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The [[html/attributes/dataPageSize|'''dataPageSize''']] property of the table determines the number of records displayed. You must set the '''DATAPAGESIZE''' attribute when designing the document, or set the corresponding '''dataPageSize''' property at run time for this method to have any effect.
'''Note'''  You do not need to check for boundary conditions.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
*<code>Reference</code>
*<code>[[dom/methods/lastPage|lastPage]]</code>
*<code>nextPage</code>
*<code>[[dom/methods/previousPage|previousPage]]</code>
*<code>Conceptual</code>
*<code>Introduction to Data Binding</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}