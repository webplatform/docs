{{Page_Title|MessageEvent}}
{{Flags
|State=In Progress
|Editorial notes=Not specific to WebSocket. Probably belongs somewhere in the DOM docs.
|Checked_Out=No
|High-level issues=Move Candidate
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A MessageEvent is sent to clients using WebSockets when data is received from the server. This is delivered to the listener indicated by the WebSocket object's onmessage attribute.}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=<syntaxhighlight lang="javascript">
socket.onmessage = function (event) {
  console.log(event.data);
}
</syntaxhighlight>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/WebSockets/WebSockets_reference/MessageEvent
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}