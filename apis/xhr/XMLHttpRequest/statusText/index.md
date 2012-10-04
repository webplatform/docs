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
|Description=The following script checks the status to determine if the request was successful:
|LiveURL=
|Code=
oReq.open("GET", "http://localhost/test.xml", false);
oReq.send()
if (oReq.statusText {{=}}{{=}} "OK")
   console.log(oReq.responseText);
else
   console.log(oReq.statusText);

}}}}
{{Notes_Section
|Notes=
===Remarks===
'''statusText''' was introduced in Windows Internet Explorer 7.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.7.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XMLHttpRequest</code>
*<code>status</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}