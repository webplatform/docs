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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script checks the HTTP status code to determine if the request was successful:
|LiveURL=
|Code=
if (oReq.status {{=}}{{=}} 401)
    console.log('Access denied.');
else
    console.log(oReq.responseText);
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''status''' was introduced in Windows Internet Explorer 7.
For a complete list of HTTP status codes and their meanings, see status Property (IXMLHTTPRequest).
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.7.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XMLHttpRequest</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}