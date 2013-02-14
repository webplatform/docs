{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Indicates the name of the sub-protocol the server selected.}}
{{API_Object_Property
|Property_applies_to=apis/websocket/WebSocket
|Read_only=Yes
|Javascript_data_type=String
|Return_value_description=This will be one of the strings specified in the protocols parameter when creating the WebSocket object.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Protocol negotiation is part of the '''WebSocket''' connection handshake. The protocol value is not set until the connection is established. If the client specifies one or more protocols, the server returns one or none of the protocols during the protocol negotiation in the handshake. After the connection is established, then the protocol value is either empty or set to the protocol that was accepted.
}}
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