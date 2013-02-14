{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Closes the WebSocket connection or connection attempt, if any.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=code
|Data type=unsigned short
|Description=A numeric value indicating the status code explaining why the connection is being closed. If this parameter is not specified, a default value of 1000 (indicating a normal "transaction complete" closure) is assumed.
|Optional=Yes
}}{{Method Parameter
|Name=reason
|Data type=String
|Description=A human-readable string explaining why the connection is closing. This string must be no longer than 123 bytes of UTF-8 text (not characters).
|Optional=Yes
}}
|Method_applies_to=apis/websocket/WebSocket
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''onclose''' event will return three attributes:
*'''wasClean''' (binary) - whether the connection closed cleanly.
*'''code''' (unsigned long) - code from the server.
*'''reason''' (text) - reason provided by the server.

If the ''code'' parameter is present but is not an integer equal to 1000 or in the range 3000 to 4999, this method throws an '''InvalidAccessError''' exception and aborts.
If the ''reason'' parameter is longer than 123 bytes this method throws a '''SyntaxError''' exception, and aborts.
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