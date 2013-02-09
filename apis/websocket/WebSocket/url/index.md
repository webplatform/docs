{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The URL as resolved by the constructor. This is always an absolute URL. Read only.}}
{{API_Object_Property
|Property_applies_to=apis/websocket/objects/WebSocket
|Read_only=No
|Return_value_description=The URL specifies the following details about the connection.

* Scheme ― The scheme must be “ws” or “wss”.  The “ws” scheme is insecure, while “wss” indicates a secure connection.  Pages that are served over HTTP should use “ws” WebSockets, while HTTPS pages should use “wss”.  Attempting to use a scheme other than “ws” or “wss” will cause an error.
* Host ― The host is the name or IP address of the server.
* Port ― This specifies the remote port to connect to.  If the port is not specified then a default is selected based on the scheme.  ”ws” connections default to port 80, while “wss” connections default to 443.
* Resource Name ― The resource name is the path component of the URL which follows the host/port.  This includes the URL query component (the part following a question mark), if one is present.  The resource name can be omitted, in which case it defaults to a forward slash ‘/’.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Example URLs
|Code=scheme://host:port/resource
ws://localhost:8080/echo
wss://cjihrig.com
}}
}}
{{Notes_Section
|Notes====Remarks===
You can use this property to make sure that the URL that is used for the connection is parsed the way the app expects.
|Import_Notes====Syntax===
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
*<code>[[apis/websocket/objects/WebSocket|WebSocket]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}