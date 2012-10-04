{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrProfilerMarkName|Data type=BSTR|Description=An event name. This parameter may be null.|Optional=}}
|Method_applies_to=dom/Element
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
Internet Explorer 10. This method is also available in the Web Worker global scope.
For Windows XP, this method sends an event to an event tracing session with TraceEvent; for systems after Windows XP, this method writes an event with EventWrite.
The event includes a pointer to a '''window''' object, current markup, and the event name passed as ''bstrProfilerMarkName''.
The ''bstrProfilerMarkName'' property has a 32-character limit when called from script.
This method is useful to profile real website performance by using the operating system metrics as a baseline.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
*<code>[[apis/workers/objects/WorkerGlobalScope|WorkerGlobalScope]]</code>
*<code>Windows Events</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}