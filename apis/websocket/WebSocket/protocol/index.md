{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A string indicating the name of the sub-protocol the server selected; this will be one of the strings specified in the protocols parameter when creating the WebSocket object.}}
{{API_Object_Property
|Property_applies_to=apis/websocket/objects/WebSocket
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Protocol negotiation is part of the '''WebSocket''' connection handshake. The protocol value is not set until the connection is established. If the client specifies one or more protocols, the server returns one or none of the protocols during the protocol negotiation in the handshake. After the connection is established, then the protocol value is either empty or set to the protocol that was accepted.
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