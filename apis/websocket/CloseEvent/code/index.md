{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The WebSocket connection close code provided by the server.}}
{{API_Object_Property
|Property_applies_to=apis/websocket/CloseEvent
|Read_only=Yes
|Example_object_name=
|Return_value_name=
|Javascript_data_type=unsigned short
|Return_value_description={{{!}}
! Status code 
! Name    
! Description
{{!}}-
{{!}} 0-999       
{{!}} 
{{!}} Reserved and not used.
{{!}}-
{{!}} 1000    
{{!}} CLOSE_NORMAL    
{{!}} Normal closure; the connection successfully completed whatever purpose for which it was created.
{{!}}-
{{!}} 1001    
{{!}} CLOSE_GOING_AWAY    
{{!}} The endpoint is going away, either because of a server failure or because the browser is navigating away from the page that opened the connection.
{{!}}-
{{!}} 1002    
{{!}} CLOSE_PROTOCOL_ERROR    
{{!}} The endpoint is terminating the connection due to a protocol error.
{{!}}-
{{!}} 1003    
{{!}} CLOSE_UNSUPPORTED   
{{!}} The connection is being terminated because the endpoint received data of a type it cannot accept (for example, a text-only endpoint received binary data).
{{!}}-
{{!}} 1004    
{{!}} CLOSE_TOO_LARGE 
{{!}} The endpoint is terminating the connection because a data frame was received that is too large.
{{!}}-
{{!}} 1005    
{{!}} CLOSE_NO_STATUS Reserved.  
{{!}} Indicates that no status code was provided even though one was expected.
{{!}}-
{{!}} 1006    
{{!}} CLOSE_ABNORMAL  Reserved. 
{{!}} Used to indicate that a connection was closed abnormally (that is, with no close frame being sent) when a status code is expected.
{{!}}-
{{!}} 1007-1999
{{!}}        
{{!}} Reserved for future use by the WebSocket standard.
{{!}}-
{{!}} 2000-2999
{{!}}        
{{!}} Reserved for use by WebSocket extensions.
{{!}}-
{{!}} 3000-3999
{{!}}        
{{!}} Available for use by libraries and frameworks. May not be used by applications.
{{!}}-
{{!}} 4000-4999
{{!}}        
{{!}} Available for use by applications.
{{!}}}
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C WebSocket Specification
|URL=http://www.w3.org/TR/websockets/
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, WebSocket}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/CloseEvent
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
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
|Safari_version=6.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
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
|Safari_mobile_version=6.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}