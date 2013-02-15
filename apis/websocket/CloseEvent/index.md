{{Page_Title|CloseEvent}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Object representing the close event for a WebSocket.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=<syntaxhighlight lang="javascript">
socket.onclose = function(event) {
  var code = event.code;
  var reason = event.reason;
  var wasClean = event.wasClean;
  // handle close event
};
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes=When a WebSocket connection is closed, possibly cleanly, the user agent must create an [[apis/websocket/WebSocket/onclose{{!}}event]] that uses the CloseEvent interface, with the event name close, which does not bubble, is not cancelable, has no default action, whose [[apis/websocket/CloseEvent/wasClean{{!}}wasClean]] attribute is set to true if the connection closed cleanly and false otherwise, whose code attribute is set to the WebSocket connection close code, and whose [[apis/websocket/CloseEvent/reason{{!}}reason]] attribute is set to the WebSocket connection close reason; and then queue a task to first change the [[apis/websocket/WebSocket/readyState{{!}}readyState]] attribute's value to CLOSED (3), and then [[apis/websocket/WebSocket/onclose{{!}}dispatch the event]] at the [[apis/websocket/WebSocket{{!}}WebSocket object]].
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
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}