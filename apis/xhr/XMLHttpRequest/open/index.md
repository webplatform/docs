{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=method
|Data type=String
|Description='''String''' that specifies the HTTP method used to open the connection: such as GET, POST, or HEAD. This parameter is not case-sensitive.
|Optional=No
}}{{Method Parameter
|Name=url
|Data type=String
|Description='''String''' that specifies either the absolute or a relative URL of the XML data or server-side Web services.
|Optional=No
}}{{Method Parameter
|Name=async
|Data type=Boolean
|Description='''Boolean''' that specifies 
true for asynchronous operation (the call returns immediately), or 
false for synchronous operation. 
If true, assign a callback handler to 
the '''onreadystatechange''' property 
to determine when the call has completed. 
If not specified, the default is true.
|Optional=No
}}{{Method Parameter
|Name=user
|Data type=String
|Description='''String''' that specifies the name of the user for authentication. If this parameter is null ("") or missing and the site requires authentication, the browser displays a logon window.
|Optional=No
}}{{Method Parameter
|Name=password
|Data type=String
|Description='''String''' that specifies the password for authentication. This parameter is ignored if the user parameter is null ("") or missing.
|Optional=No
}}
|Method_applies_to=apis/xhr/objects/XMLHttpRequest
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
'''open''' was introduced in Windows Internet Explorer 7.
The following 
HTTP verbs and 
World Wide Web Distributed Authoring and Versioning (WebDAV) methods are supported:
{| class="wikitable"
|-
!Verb / Method
!Defined In [http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP  (RFC-2616)]
!Defined In [http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV (RFC-2518)]
!Function
|-
|GET
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Request URI
|-
|POST
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Send data to server
|-
|HEAD
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Request URI without body
|-
|PUT
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Store data for URI
|-
|DELETE
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Delete data for URI
|-
|MOVE
|
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Move URI to to new location
|-
|PROPFIND
|
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Request URI Properties
|-
|PROPPATCH
|
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Update or Delete URI Properties
|-
|MKCOL
|
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Create collection at URI
|-
|COPY
|
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Create copy of URI
|-
|LOCK
|
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Create Lock
|-
|UNLOCK
|
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Remove Lock
|-
|OPTIONS
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
|[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
|Request URI Options
|}
 
Internet Explorer caches the results of HTTP GET requests in the Temporary Internet Files (TIF) folder. In most cases, caching improves performance for data that will not change frequently. To guarantee that the results are not cached, use POST.
'''Security Warning:  ''' Cross-domain, cross-port, and mixed protocol requests are not allowed. The ''bstrUrl'' parameter may only specify files in the same domain, using the same port and protocol method, as that from which the page is served.
Although this method accepts credentials passed via parameter, those credentials are not automatically sent to the server on the first request. The ''varUser'' and ''varPassword'' parameters are not transmitted unless the server challenges the client for credentials with a 401 - Access Denied response.
After calling this method, use '''send''' to send the request and data, if any, to the server.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203789 XMLHttpRequest], Section 3.6.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>XMLHttpRequest</code>
*<code>Reference</code>
*<code>abort</code>
*<code>onreadystatechange</code>
*<code>Other Resources</code>
*<code>Communicating XML Data over the Web with WebDAV</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}