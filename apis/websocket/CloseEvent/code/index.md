{{Page_Title|code}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=apis/websockets/CloseEvent
|Read_only=No
|Javascript_data_type=unsigned long
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
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
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
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/CloseEvent
|MSDN_link=
|HTML5Rocks_link=
}}