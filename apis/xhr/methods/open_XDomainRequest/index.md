{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrMethod|Data type=BSTR|Description=[http://go.microsoft.com/fwlink/?linkid{{=}}84048 GET] method.


[http://go.microsoft.com/fwlink/?linkid{{=}}84048 POST] method.

|Optional=}}
{{Method Parameter|Name=bstrUrl|Data type=BSTR|Description=The server [http://go.microsoft.com/fwlink/?linkid{{=}}203716 URL.]|Optional=}}
|Method_applies_to=apis/xhr/objects/XDomainRequest
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
|Description=
|LiveURL=
|Code=
  
// 1. Create XDR object 
xdr {{=}} new XDomainRequest(); 

// 2. Open connection with server using POST method
xdr.open("POST", "http://www.contoso.com/xdr.txt");

// 3. Send string data to server
xdr.send("data to be processed");     
                
}}}}
{{Notes_Section
|Notes=
===Remarks===
Requires an XDomainRequest object.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>IHTMLXDomainRequest</code>
*<code>XDomainRequest</code>
*<code>Other Resources</code>
*<code>[http://go.microsoft.com/fwlink/?linkid{{=}}203716 W3C Architecture: Naming and Addressing: URIs, URLs, ...]</code>
*<code>[http://go.microsoft.com/fwlink/?linkid{{=}}84048 RFC2616: Hypertext Transfer Protocol -- HTTP/1.1]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}