{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/xhr/objects/XMLHttpRequest
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
'''abort''' was introduced in Windows Internet Explorer 7.
The '''abort''' method interrupts an asynchronous operation in progress. (Pass true to the ''varAsync'' parameter of '''open''' to create an asynchronous request.)
Calling '''abort''' resets the object; the '''readyState''' is changed to 0 (uninitialized).
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XMLHttpRequest</code>
*<code>XDomainRequest</code>
*<code>send</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}