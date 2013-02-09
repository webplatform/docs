{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Initializes an XMLHttpRequest.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=method
|Data type=String
|Description=Specifies the HTTP method used to open the connection, such as GET, POST, or HEAD. This parameter is not case-sensitive.
|Optional=No
}}{{Method Parameter
|Name=url
|Data type=String
|Description=Specifies either an absolute or relative URL of the XML data or server-side Web services.
|Optional=No
}}{{Method Parameter
|Name=async
|Data type=Boolean
|Description=Specifies 
true for asynchronous operation (the call returns immediately), or 
false for synchronous operation. 
If true, assign a callback handler to 
the '''onreadystatechange''' property 
to determine when the call has completed. 
If not specified, the default is true.
|Optional=Yes
}}{{Method Parameter
|Name=user
|Data type=String
|Description=Specifies the name of the user for authentication. If this parameter is null or not specified and the site requires authentication, the browser displays a logon window.
|Optional=Yes
}}{{Method Parameter
|Name=password
|Data type=String
|Description=Specifies the password for authentication. This parameter is ignored if the user parameter is null or not specified.
|Optional=Yes
}}
|Method_applies_to=apis/xhr/XMLHttpRequest
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The following 
HTTP verbs and 
World Wide Web Distributed Authoring and Versioning (WebDAV) methods are supported:
{{{!}} class="wikitable"
{{!}}-
!Verb / Method
!Defined In [http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP  (RFC-2616)]
!Defined In [http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV (RFC-2518)]
!Function
{{!}}-
{{!}}GET
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Request URI
{{!}}-
{{!}}POST
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Send data to server
{{!}}-
{{!}}HEAD
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Request URI without body
{{!}}-
{{!}}PUT
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Store data for URI
{{!}}-
{{!}}DELETE
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Delete data for URI
{{!}}-
{{!}}MOVE
{{!}}
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Move URI to to new location
{{!}}-
{{!}}PROPFIND
{{!}}
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Request URI Properties
{{!}}-
{{!}}PROPPATCH
{{!}}
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Update or Delete URI Properties
{{!}}-
{{!}}MKCOL
{{!}}
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Create collection at URI
{{!}}-
{{!}}COPY
{{!}}
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Create copy of URI
{{!}}-
{{!}}LOCK
{{!}}
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Create Lock
{{!}}-
{{!}}UNLOCK
{{!}}
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Remove Lock
{{!}}-
{{!}}OPTIONS
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84048 HTTP]
{{!}}[http://go.microsoft.com/fwlink/p/?linkid{{=}}84046 WebDAV]
{{!}}Request URI Options
{{!}}}

Internet Explorer caches the results of HTTP GET requests in the Temporary Internet Files (TIF) folder. In most cases, caching improves performance for data that will not change frequently. To guarantee that the results are not cached, use POST.
'''Security Warning:  ''' Cross-domain, cross-port, and mixed protocol requests are not allowed. The ''bstrUrl'' parameter may only specify files in the same domain, using the same port and protocol method, as that from which the page is served.
Although this method accepts credentials passed via parameter, those credentials are not automatically sent to the server on the first request. The ''varUser'' and ''varPassword'' parameters are not transmitted unless the server challenges the client for credentials with a 401 - Access Denied response.
After calling this method, use '''send''' to send the request and data, if any, to the server.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C XMLHttpRequest Specification
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=23.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=3.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|XHR}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}