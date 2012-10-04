{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=urls|Data type=DOMString|Description=|Optional=}}
|Method_applies_to=apis/workers/objects/WorkerNavigator
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

S_OK

Type: '''HRESULT'''

This method can return one of these values.

S_OK


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The URL that is loaded must resolve according to the [[apis/workers/objects/WorkerLocation|'''WorkerLocation''']] of the worker. More than one script can be loaded in a sequence of URLs. The loading and executing of scripts is synchronous. If any script throws an exception, subsequent scripts will not load.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/workers/objects/WorkerGlobalScope|WorkerGlobalScope]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}