{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The current state of the connection, represented as a numeric constant.}}
{{API_Object_Property
|Property_applies_to=apis/websocket/WebSocket
|Read_only=Yes
|Javascript_data_type=unsigned short
|Return_value_description=These constants are used by the readyState attribute to describe the state of the WebSocket connection.

{{{!}}
! Constant
! Value
! Description
{{!}}-
{{!}} CONNECTING
{{!}} 0 
{{!}} The connection is not yet open.
{{!}}-
{{!}} OPEN       
{{!}} 1
{{!}} The connection is open and ready to communicate.
{{!}}-
{{!}} CLOSING    
{{!}} 2 
{{!}} The connection is in the process of closing.
{{!}}-
{{!}} CLOSED     
{{!}} 3 
{{!}} The connection is closed or couldn't be opened.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=switch (socket.readyState) {
  case WebSocket.CONNECTING:
    // do something
    break;
  case WebSocket.OPEN:
    // do something
    break;
  case WebSocket.CLOSING:
    // do something
    break;
  case WebSocket.CLOSED:
    // do something
    break;
  default:
    // this never happens
    break;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C WebSocket Specification
|URL=http://www.w3.org/TR/websockets/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|WebSocket}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/WebSocket
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}