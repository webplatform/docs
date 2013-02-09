{{Page_Title|CloseEvent}}
{{Flags
|High-level issues=Needs Topics
|Content=Cleanup, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|When the WebSocket connection is closed, possibly cleanly, the user agent must create an [[apis/websocket/events/onclose{{!}}event]] that uses the CloseEvent interface, with the event name close, which does not bubble, is not cancelable, has no default action, whose [[apis/websocket/CloseEvent/wasClean{{!}}wasClean]] attribute is set to true if the connection closed cleanly and false otherwise, whose code attribute is set to the WebSocket connection close code, and whose [[apis/websocket/CloseEvent/reason{{!}}reason]] attribute is set to the WebSocket connection close reason; and queue a task to first change the [[apis/websocket/properties/readyState{{!}}readyState]] attribute's value to CLOSED (3), and then [[apis/websocket/events/onclose{{!}}dispatch the event]] at the [[apis/websocket/objects/WebSocket{{!}}WebSocket object]].}}
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}