{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/xhr/objects/XMLHttpRequest
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
You cannot call [[apis/xhr/properties/responseBody|'''responseBody''']] and '''responseText''' properties to obtain partial results ('''readyState''' {{=}} 3). Doing so will return an error, because  the response is not fully received. You must wait until all data has been received.
In comparison, the Microsoft XML (MSXML) version of the [[apis/xhr/properties/responseBody|'''responseBody''']] and '''responseText'''.
In comparison, the MSXML version of the [[apis/xhr/properties/responseBody|'''responseBody''']] and '''responseText'''.
For an example of how to use this property, see [[apis/xhr/events/readystatechange|'''onreadystatechange''']].
'''readyState''' was introduced in Windows Internet Explorer 7.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XMLHttpRequest</code>
*<code>onreadystatechange</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}