{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|An event handler that is fired when changes are made to the active history. Calls to pushState or replaceState can trigger this event.}}
{{Event
|Event_applies_to=dom/PopStateEvent
|Synchronous=No
|Bubbles=Yes
|Target=dom/Element
|Cancelable=No
|Default_action=None
|Interface=dom/PopStateEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=window.onpopstate {{=}} function(evt) {
  alert("location: " + document.location + ", state: " + JSON.stringify(evt.state));
};
history.pushState({page: 1}, "title 1", "?page=1");
history.pushState({page: 2}, "title 2", "?page=2");
history.replaceState({page: 3}, "title 3", "?page=3");
history.back(); // alerts "location: http://example.com/example.html?page=1, state: {"page":1}"
history.back(); // alerts "location: http://example.com/example.html, state: null
history.go(2);  // alerts "location: http://example.com/example.html?page=3, state: {"page":3}
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Event handler parameters===
;''val'' [in]:Type: '''Function''' A script function to do something when the event is fired.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/Events/popstate popstate]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh771875(v=vs.85).aspx popstate Event]
|HTML5Rocks_link=
}}