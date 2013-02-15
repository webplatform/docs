{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|An event listener to be called when an error occurs. Receives an event named "error".}}
{{API_Object_Property
|Property_applies_to=apis/websocket/WebSocket
|Read_only=Yes
|Return_value_description=EventHandler
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=socket.onerror = function(event) {
  // handle error event
};
}}{{Single Example
|Language=JavaScript
|Description=An equivalent "onerror" event handler that uses the addEventListener() method.
|Code=socket.addEventListener("error", function(event) {
  // handle error event
});
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
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}