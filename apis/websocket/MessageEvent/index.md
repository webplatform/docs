{{Page_Title|MessageEvent}}
{{Flags
|High-level issues=Move Candidate
|Editorial notes=Not specific to WebSocket. Probably belongs somewhere in the DOM docs.
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|A MessageEvent is sent to clients using WebSockets when data is received from the server. This is delivered to the listener indicated by the WebSocket object's onmessage attribute.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=<syntaxhighlight lang="javascript">
socket.onmessage = function (event) {
  console.log(event.data);
}
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
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/MessageEvent
|MSDN_link=
|HTML5Rocks_link=
}}