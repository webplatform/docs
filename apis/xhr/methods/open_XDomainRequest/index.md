{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status. Probably should be renamed to remove (XDomainRequest) from the URL.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=bstrMethod
|Data type=BSTR
|Description=GET method.

POST method.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=bstrUrl
|Data type=BSTR
|Description=The server URL.
|Optional=No
}}
|Method_applies_to=apis/xhr/objects/XDomainRequest
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=// 1. Create XDR object 
xdr {{=}} new XDomainRequest(); 

// 2. Open connection with server using POST method
xdr.open("POST", "http://www.contoso.com/xdr.txt");

// 3. Send string data to server
xdr.send("data to be processed");
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Requires an XDomainRequest object.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>IHTMLXDomainRequest</code>
*<code>XDomainRequest</code>
*<code>Other Resources</code>
*<code>[http://go.microsoft.com/fwlink/?linkid{{=}}203716 W3C Architecture: Naming and Addressing: URIs, URLs, ...]</code>
*<code>[http://go.microsoft.com/fwlink/?linkid{{=}}84048 RFC2616: Hypertext Transfer Protocol -- HTTP/1.1]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}