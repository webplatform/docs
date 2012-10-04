{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrHeader|Data type=BSTR|Description='''String''' that specifies the header name.|Optional=}}
{{Method Parameter|Name=bstrValue|Data type=BSTR|Description='''String''' that specifies the header value.|Optional=}}
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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following script sets the HTTP Content-Type header to 'text/xml' before sending the request body:
|LiveURL=
|Code=
var oReq {{=}} new XMLHttpRequest();
oReq.open("POST", sURL, false);
oReq.setRequestHeader("Content-Type", "text/xml");
oReq.send(sRequestBody);
}}}}
{{Notes_Section
|Notes=
===Remarks===
Refer to [http://go.microsoft.com/fwlink/p/?linkid{{=}}203727 RFC2616, Section 14: Header Field Definitions] for a general list of standard headers. The server is ultimately responsible for honoring the headers of the request. By far the most common request header is Content-Type, which is required by some XML Web services.
'''setRequestHeader''' was introduced in Windows Internet Explorer 7.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.6.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>XMLHttpRequest</code>
*<code>getResponseHeader</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}